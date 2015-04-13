## Advanced scraper construction

### Contents

1. downloading linked files
2. regular expressions
3. following links

#### Downloading linked files

- ***download*** - if present and has a truthey value (`true` or an Object) the element is treated as a URL to a resource and is downloaded. **Optional** (omitting this key is equivalent to giving it a value of `false`). If the value is an object, the following keys are allowed:
    - `rename` - a string specifying the filename to which the downloaded file will be renamed.

Example:
```json
{
  "url": "plos.*\\.org",
  "elements": {
    "fulltext_pdf": {
      "selector": "//meta[@name='citation_pdf_url']",
      "attribute": "content",
      "download": {
        "rename": "fulltext.pdf"
      }
    },
    "title": {
      "selector": "//meta[@name='citation_title']"
    }
  }
}
```

#### Regular expressions

- ***regex*** - an Object specifying a regular expression whose groups should be captured as the results. The results will be an array of the captured groups. If the global flag (`g`) is specified, the result will be an array of arrays of captured groups. There are two keys allowed:
    - `source` - a string specifying the regular expression to be executed. **Required**
    - `flags` - an array specifying the regex flags to be used (`g`, `m`, `i`, etc.). **Optional** (omitting this key will cause the regex to be executed with no flags).

Example:
```json
{
  "url": "plos.*\\.org",
  "elements": {
    "fulltext_pdf": {
      "selector": "//meta[@name='citation_pdf_url']",
      "attribute": "content",
      "regex": {
        "flags": ["g", "m"],
        "source": "(\\w+)"
      },
      "download": {
        "rename": "fulltext.pdf"
      }
    },
    "title": {
      "selector": "//meta[@name='citation_title']"
    }
  }
}
```

### Following links

Sometimes the content you want to scrape from a page requires clicking on a link from that page before you can access it. For example, when reading a scientific article, if you want to look at the full-resolution version of a figure, you might need to click a 'view full size' link, that will open a new page that displays the image.

ScraperJSON accomodates this by using the concept of 'following' scraped links. To use following, you include at least two selectors: one for the link you want to follow, and one for each element you want to scrape once the link has been followed. You tell ScraperJSON about the following relationship by annotating the 'follower':

Example:
```json
{
  "url": "plos.*\\.org",
  "elements": {
    "figure_fullpage": {
      "selector": "//a[@class='full-figure']",
      "attribute": "href"
    },
    "figure_image": {
      "selector": "//a[@name='fullsize-image']",
      "attribute": "href",
      "follow": "figure_fullpage"
    }
  }
}
```
