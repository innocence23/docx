Docx Parser
====

This PHP based parser takes any docx file, and creates a PHP array containing its structure, content &amp; style information.
Simply import any style data (as demonstrated within index.php) using the word style name & any desired attributes and run the parser.

====

Supports:
- Word styles
- Paragraphs
- Text indentation / tabbing
- Nested lists (&amp; inline lists)
- Tables (Vertical cell merging + colspans)
- Images (&amp; finding the required image size)
- Hyperlinks (With mailto: support)
- Bold / Underlined / Italic text
- Textboxes (Parser support added, but not rendered)
- Table of content functionality (You likely need to extend the docx class & modify the ->render() class)

====

Caveats:

- Images are displayed at the same dimensions as in word, however the included rendering class does not contain functionality for resizing the raw image files as required (due to it being out of scope for this project)
- The parser may take some time to run on larger documents
- Modifying text in word to look the same as a header style is not the same as setting its stylename to 'header'

====

Requirements:

- PHP 5.3 or greater
- /tmp writable by PHP
