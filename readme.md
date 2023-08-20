# ePubExport MediaWiki Extension

The `ePubExport` extension allows users to export MediaWiki articles or content to the ePub format, suitable for reading on various eReader devices. Users can specify a list of pages and an associated image for the export.

## Overview

- **ePubExport_body.php**: Contains the main logic for exporting MediaWiki content to ePub. It defines the `SpecialePub` class which extends MediaWiki's `SpecialPage` class.
- **ePubExport.i18n.php**: An internationalization file that provides multilingual support for the extension.
- **ePubExport.php**: The main configuration and setup file for integrating the `ePubExport` functionality into MediaWiki.
- **ePubExport.i18n.alias.php**: Provides aliases in multiple languages for accessing the special ePubExport page.
- **ebook.css**: A CSS stylesheet for styling the content within the exported ePub to ensure consistent appearance across eReader devices.
- **EPub.php**: A class that facilitates the creation of ePub-compatible book files.
- **EPubChapterSplitter.php**: This class is designed to split larger HTML files into smaller chapters while retaining formatting and structure.
- **Zip.php**: A utility class for creating and managing Zip archive files, essential for ePub generation since ePub files are essentially Zip archives.

## Installation

1. Download and place the files in a directory called `ePubExport` in your `extensions/` folder.
2. Add the following code at the bottom of your `LocalSettings.php`: `wfLoadExtension( 'ePubExport' );`

Navigate to "Special:ePubExport" on your wiki to access the functionality.

## Configuration

- Set `$wgePubExportHttpsImages` to `true` if your MediaWiki page is on an HTTPS server and contains images that are available over both HTTPS and HTTP.
- To set a default cover image for the ePub export, use: `$wgePubExportProperties['cover_image'] = '/path/to/image/image.jpg';`
- To embed TTF fonts in the ePub file, use: `$wgePubExportProperties['embed_fonts'] = true;`

## Usage

1. Navigate to the page you wish to export.
2. Click on the "ePub Export" link (or the equivalent in your language) to start the export process.
3. Specify a list of pages you want to include in the ePub export.
4. Optionally, provide an image that will be used as the cover or associated image for the exported ePub.
5. Download the generated ePub file.

## Contributing

Translations, bug reports, and improvements are welcome! Please open an issue or submit a pull request on the GitHub repository.




