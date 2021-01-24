# Blog Pages

This repository contains raw blog page files to be programmatically processed into webpages and a specification of how to write those page files.

## Metadata

Page metadata is provided as a series of key-value pairs at the **top** of each page.

The page's metadata listing is separated from its page content by a line containing **only** dashes. The separating line may contain any number of dashes as long as it only contains dashes. Additionally, the line may be trailed by an arbitrary amount of white-space.

    $key=DATA
    $other-key=OTHER DATA
    ---
    The page's actual content

As the metadata is contained in the raw page source, page view implementations are expected to remove or preprocess the metadata before rendering the page.

Provided is a table defining the standard types of metadata. Implementations are expected to handle future additions to the table without breakage.

| Key        | Meaning                                |
| ---------- | -------------------------------------- |
| `$title`   | Title of the page                      |
| `$summary` | A brief summary of the page's contents |
| `$date`    | mm/dd/yyyy formatted date string       |

## Indexing

Each page is indexed in the `page-listing.json`. The index contains a listing of each page's metadata, as well as additional information such as the page's file path.

## Scripts

[pre-commit](hooks/pre-commit) is a script which scans all relevant blog page files for page metadata and produces a `page-listing.json` file used for indexing all pages in a blog.

Whenever the file is updated, it should be copied into the `.git/hooks` directory.
