**Fulcrum EPUB Specification**

**Revision History**

<table>
<thead>
<tr class="header">
<th><strong>Rev Num</strong></th>
<th><strong>Release Date</strong></th>
<th><strong>Changes </strong></th>
<th><strong>Author</strong></th>
</tr>
</thead>
<tbody>
<tr class="even">
<td>1.2</td>
<td>Jan. 15, 2020</td>
<td>HELIO-3146</td>
<td>tbelc@umich.edu</td>
</tr>
<tr class="odd">
<td>1.1</td>
<td>May 14, 2019</td>
<td>HELIO-2661</td>
<td>tbelc@umich.edu</td>
</tr>
<tr class="even">
<td>1.0</td>
<td>May. 12, 2018</td>
<td><p>Beta Release to UM</p>
<p>Full Spec Internal</p></td>
<td>Arthic Leo A E</td>
</tr>
<tr class="odd">
<td>1.0b1</td>
<td>July 16, 2018</td>
<td>Beta release version 2.0</td>
<td>Arthic Leo A E</td>
</tr>
<tr class="even">
<td>1.0b2</td>
<td>July 24, 2018</td>
<td>Beta release version 3.0</td>
<td>Arthic Leo A E</td>
</tr>
<tr class="odd">
<td>1.0b3</td>
<td>July 24, 2018</td>
<td>Beta release version 3.0</td>
<td>G Suprock</td>
</tr>
<tr class="even">
<td>1.0b4</td>
<td>Aug. 21, 2018</td>
<td>Beta release version 4.0</td>
<td>G Suprock</td>
</tr>
<tr class="odd">
<td>1.1rc1</td>
<td>Sept 20, 2018</td>
<td>Release candidate 1.0</td>
<td>J McGlone</td>
</tr>
<tr class="even">
<td>2.0</td>
<td>Dec 20, 2018</td>
<td>Release to web</td>
<td>J McGlone</td>
</tr>
<tr class="odd">
<td>2.1</td>
<td>Feb 7, 2018</td>
<td>Removed non-spec material, added code block spec (1.16)</td>
<td>J McGlone</td>
</tr>
</tbody>
</table>

**Contents**

[1.0 Target Specification -- EPUB3 1-1](#_Toc441165)

[1.1 EPUB Version 1-1](#epub-version)

[1.2 Element Specification 1-1](#element-specification)

[1.2.1 Standard Functionality Levels (ePub 3) for PDF source
1-1](#standard-functionality-levels-epub-3-for-pdf-source)

[1.3 File Name 1-2](#file-name)

[1.4 Folder Structure 1-2](#folder-structure)

[1.4.1 Optional File Inclusions 1-3](#optional-file-inclusions)

[1.5 EPUB Package 1-3](#epub-package)

[1.6 Metadata 1-4](#metadata)

[1.6.1 Dublin Core 1-4](#dublin-core)

[1.7 Accessibility Metadata 1-5](#accessibility-metadata)

[1.8 HTML Meta Header 1-5](#html-meta-header)

[1.9 Bookmark 1-5](#bookmark)

[1.10 Html Title 1-6](#html-title)

[1.11 Headings 1-6](#headings)

[1.11.1 Numbered headings 1-6](#numbered-headings)

[1.11.2 Separate heading and subtitle
1-6](#separate-heading-and-subtitle)

[1.11.3 Merged heading and subtitle 1-7](#merged-heading-and-subtitle)

[1.12 Tables 1-7](#tables)

[1.12.1 Irregular header 1-7](#irregular-header)

[1.12.2 Complex headings 1-8](#complex-headings)

[1.12.3 Layered headings 1-8](#layered-headings)

[1.13 Lists 1-9](#lists)

[1.13.1 Unordered list 1-9](#unordered-list)

[1.13.2 Definition list 1-10](#definition-list)

[1.14 Links 1-10](#links)

[1.14.1 Links spec 1-10](#links-spec)

[1.14.2 Link with full context of destination
1-10](#link-with-full-context-of-destination)

[1.14.3 Link with alternate text 1-11](#link-with-alternate-text)

[1.14.4 Visual distinctive linking 1-11](#visual-distinctive-linking)

[1.15 Images 1-11](#images)

[1.15.1 Significant simple image (no description required)
1-11](#significant-simple-image-no-description-required)

[1.15.2 Extended description via hyperlink
1-11](#extended-description-via-hyperlink)

[1.15.3 Decorative image 1-12](#decorative-image)

[1.16 Code Blocks 1-12](#code-blocks)

[1.16.1 Inline Code 1-12](#inline-code)

[1.16.2 Code Blocks 1-13](#code-blocks-1)

[1.16.3 Code Blocks with Line Numbers
1-13](#code-blocks-with-line-numbers)

[1.16.4 Code Blocks with Line Numbers as Tables
1-14](#code-blocks-with-line-numbers-as-tables)

[1.16.5 Comparing Code Blocks with Line Numbers
1-15](#comparing-code-blocks-with-line-numbers)

[1.17 Footnotes and Endnotes 1-16](#footnotes-and-endnotes)

[1.17.1 Footnotes in the body 1-16](#footnotes-in-the-body)

[1.17.2 Endnote section 1-16](#endnote-section)

[1.17.3 Back-linking notes 1-17](#back-linking-notes)

[1.18 Content Numbering 1-17](#content-numbering)

[1.18.1 Page Break Numbering 1-17](#page-break-numbering)

[1.18.2 Paragraph Numbering 1-17](#paragraph-numbering)

[1.18.3 Line Numbering 1-17](#line-numbering)

[1.19 Chapter Split 1-17](#chapter-split)

[1.20 CSS Stylesheet 1-18](#css-stylesheet)

[1.20.1 Standard CSS 1-18](#standard-css)

[1.20.2 CSS Units 1-18](#css-units)

[1.20.3 Colors 1-18](#colors)

[1.20.4 Background Images 1-18](#background-images)

[1.20.5 Hidden Content 1-19](#hidden-content)

[1.20.6 CSS Property Reference 1-19](#css-property-reference)

[1.20.7 CSS 2.1 1-19](#css-2.1)

[1.20.8 CSS 2.1 Pseudo-Classes 1-25](#css-2.1-pseudo-classes)

[1.20.9 CSS 2.1 Pseudo-Elements 1-26](#css-2.1-pseudo-elements)

[1.21 Images 1-27](#images-1)

[1.21.1 Image File Types 1-27](#image-file-types)

[1.21.2 Recommended Criteria 1-27](#recommended-criteria)

[1.21.3 Cover Image 1-27](#cover-image)

[1.21.4 Image/Graphic Placement 1-28](#imagegraphic-placement)

[1.22 Fonts 1-28](#fonts)

[1.23 Formatting 1-28](#formatting)

[1.24 Boxed Text 1-28](#boxed-text)

[1.25 Marginalia and Sidebars 1-29](#marginalia-and-sidebars)

[1.26 Reading Order 1-29](#reading-order)

[1.27 DPUB ARIA Semantics 1-29](#dpub-aria-semantics)

[1.28 Accessibility 1-31](#accessibility)

Target Specification -- EPUB3
=============================

EPUB Version
------------

EPUB version 3.0.1 is the recommended technical specification for EPUB
created for submission to Fulcrum. Please note this document does not
repeat conformance requirements contained in the official specification.
However, recommended features regarding file and directory structure,
naming conventions, treatments for images, treatments for metadata, and
other such file preparation details are included.

The full EPUB 3.0.1 specification is located here:
[[http://idpf.org/epub/301](http://idpf.org/epub/301).

-   International Digital Publishing Form (IDPF) guidelines for
    reflowable digital books and publications.

-   ePub validated against ePubCheck version 4.0.2
    (<http://code.google.com/p/epubcheck/>)

-   XHTML files compliant with XHTML 1.1 DTD

-   XHTML files validated with CSE HTML validator version 10.0

Element Specification
---------------------

The following matrix details recommendations how to convert different
elements. The treatments are optional for third-party partners to
University of Michigan.

### Standard Functionality Levels (ePub 3) for PDF source

| **Element**                   | **Conversion**                           |
| ----------------------------- | ---------------------------------------- |
| Parts/Chapters                | All Heading Levels                       |
| Graphics + Captions           | Image + Text                             |
| Tables + Captions             | Text                                     |
| Sidebars                      | Text                                     |
| Display Math                  | MathML                                   |
| In-line Math                  | Text (if keyable) / MathML (non-keyable) |
| Lists                         | Text                                     |
| Footnotes/Endnotes            | Bi-directional text                      |
| Poems                         | Text                                     |
| Plays/Dialog                  | Text                                     |
| Non-keyboard Characters       | Unicode                                  |
| Drop cap                      | Text                                     |
| Cover                         | Image                                    |
| Title Page                    | Text                                     |
| About the Author              | Text                                     |
| Acknowledgements              | Text                                     |
| Copyright Page                | Text                                     |
| Table of Contents             | Bi-directional                           |
| Lists of Tables/Figs, etc.    | Text with bi-directional links           |
| Dedications/Epigraphs         | Text                                     |
| Foreword/Introduction/Preface | Text                                     |
| References/Bibliography       | Text                                     |
| Glossary/Appendix             | Text                                     |
| Index                         | Text with links                          |

**<span class="underline">Note</span>:** If the input is ePub, then output should be in
the same format.

File Name
---------

The EPUB3 output file name will be the 13-digit ISBN number of the same
input file name for Apex Production.

The use of the 13-digit ISBN number of the source file is optional for
third-party partners to University of Michigan. However, file naming
conventions must be consistent across titles submitted to the
university.

Folder Structure
----------------

The following folder structure is required for Apex deliverables to the
University of Michigan. The folder structure below is optional for
third-party partners to University of Michigan. However, folder
structure conventions must be consistent across titles submitted to the
university.

The EPUB should conform to the following directory structure and naming
convention.

<pre>
<b>/META-INF</b>
    <b>container.xml</b>
<b>/OEBPS</b>
    <b>/xhtml/<i>xxy_Filename</i>.xhtml</b>
    <b>content.opf</b>
    <b>/fonts</b>
        <b><i>Fontname</i>.<i>fontextension</i></b>
    <b>/images</b>
        <b>cover.<i>imgextension</i></b>
        <b><i>figname</i>.<i>imgextension</i></b>
    <b>/styles</b>
        <b>page-template.xpgt</b>
        <b><i>stylesheet</i>.css</b>
    <b>toc.ncx</b>
<b>mimetype</b>
</pre>

Where,

<pre>
<b><i>xx</i></b> = A sequential numeric book part identifier beginning with 00 and incrementing by 1 (e.g., 00, 01, 02, 03, and so on)
<b><i>y</i></b> = An optional alphabetic section identifier used when book parts contain large numbers of image files (e.g., 01a, 01b, 01c, and so on)
<b><i>Filename</i></b> = A human readable book part name (e.g., Nav, Cover, Title, Contents, Chapter01
<b><i>Fontname</i></b> = A font file name (e.g., MinionPro-Regular)
<b><i>fontextension</i></b> = A font file extension (e.g., ttf)
<b><i>figname</i></b> = Figure name. Please do not modify this name, as it may be an identifier for accessing associated metadata.
<b><i>imgextension</i></b> = An image file extension (e.g., jpg, png)
<b><i>stylesheet</i></b> = A human readable CSS stylesheet name.
</pre>

### Optional File Inclusions

Additional inclusions supporting alternative EPUB Reader systems, such
as ibooks and the com.apple.ibooks.display-options.xml file, is
permissible and will not interfere with the Fulcrum viewer.

If such files are in source, they will be in the deliverable EPUB3.

EPUB Package
------------

The EPUB3 output contains the following folders and files.

-   XHTML files

-   Image files

-   toc.ncx

-   mimetype

-   container.xml

-   content.opf

-   Stylesheet (CSS)

-   Embedded Fonts (Only if approved by customer)

Metadata
--------

### Dublin Core

Dublin Core metadata is required for the following items:

-   Title

-   Creator

-   Language

-   Rights

-   Publisher

-   Identifier

-   Source (Required when the EPUB is a derivative of a print source.)

**Example code:**

<pre>
&lt;dc:title>A Mid-Republican House from Gabii&lt;/dc:title>
&lt;dc:creator>Rachel Opitz&lt;/dc:creator>
&lt;dc:creator>Marcello Mogetta&lt;/dc:creator>
&lt;dc:creator>Nicola Terrenato&lt;/dc:creator>
&lt;dc:language>en-US&lt;/dc:language>
&lt;dc:rights>© University of Michigan Press&lt;/dc:rights>
&lt;dc:publisher>University of Michigan Press&lt;/dc:publisher>
&lt;dc:identifier id="BookID">9780472999002&lt;/dc:identifier>
&lt;dc:sourceid="src-id">urn:isbn:9780472999999&lt;/dc:source>
&lt;meta refines="#src-id" property="dcterms:issued">2000-01-01&lt;/meta>
&lt;dc:date>2018-03-03&lt;/dc:date>
</pre>

Accessibility Metadata
----------------------

Include the two types of accessibility metadata structure defined in the
current EPUB environment as listed below.

> ONIX: <http://kb.daisy.org/publishing/docs/metadata/onix.html>

Use ONIX only when creating a separate ONIX metadata XML to place in
the /meta folder of the EPUB.

> Schema: <http://kb.daisy.org/publishing/docs/metadata/schema-org.html>

HTML Meta Header
----------------

For Apex created EPUBs, the follow meta tags will be placed inside the
\<head\> tag in all the XHTML files. The meta tags are optional for
third-party partners to University of Michigan.

<pre>
&lt;meta name="viewport" content="initial-scale=1.0,maximum-scale=5.0"/>
&lt;meta content=" " name=" " role="section"/>
</pre>
The chapter id should be provided as value for content attribute and the type of the
section should be provided under name attribute. For example:
<pre>
&lt;meta content="dedication" name="dedication" role="section"/>
&lt;meta content="chapter04" name="chapter04" role="section"/>
</pre>

## Bookmark

Bookmark each ePUB as follows:

-   Cover
-   Title
    -   Note: If there are multiple title pages, label the bookmarks
        "Title Page" and "Original Title Page".
-   Half Title
-   Copyright
    -   Note: If there are multiple copyright pages (e.g., the Routledge
        Revivals imprint which contains the original copyright page
        usually from the 1800s), the bookmarks are to be labeled
        "Copyright Page" and "Original Copyright Page".
-   Dedication
-   Table of Contents
    -   Note to Production: If the Table of Contents is missing for a
        title, raise a JIRA ticket to see if the client can resupply the
        file. If not, construct the bookmarks from the Chapter Titles.
-   All book sections listed in the Table of Contents
-   All Lists of Tables, Figures, Illustrations, Maps, etc.
-   Appendices
-   Indexes

## Html Title

HTML titles are a best practice recommendation, and, required for Apex
EPUB deliveries. However, HTML titles are optional for third-party
partners to University of Michigan.

Assigning meaningful titles is a recommended best practice for \<title\>
elements in the EPUB. Such titles help all users to find and navigate
through the documents, and, are essential for screen reader users.

Example 1 --- One chapter/part per HTML

<pre>
&lt;html ...>
&lt;title>Chapter 1 --- Hobo's Guide to the Universe&lt;/title>
</pre>

Example 2 --- Multiple HTML files for one chapter/part

If a document is split into multiple HTML files, the following method
should be followed.

<pre>
&lt;html ...>
&lt;title>Chapter 1 - Continued (2 of 3) --- Hobo's Guide to the Universe&lt;/title>
</pre>

Headings
--------

Apply heading tags as per the HTML element for the headings. Based on
the heading levels, apply heading tags ranging from h1 to h6 as needed.

### Numbered headings

<pre>
&lt;section role="doc-part">
&lt;h1>Book One: 1805&lt;/h1>
&lt;section role="doc-part">
&lt;h2>Part 1&lt;/h2>
&lt;section role="doc-chapter">
&lt;h3>Chapter 1&lt;/h3>
</pre>

### Separate heading and subtitle

The title and subtitle are contained in separate elements, but grouped
in a header element to better associate them. Use the role
doc-subtitle to identify the subtitle.
<pre>
&lt;section role="doc-chapter">
&lt;header>
&lt;h1>ORIGIN OF THE WORLD.---FIRST DYNASTY.&lt;/h1>
&lt;p role="doc-subtitle">URANUS AND GÆA. (Cœlus and Terra.)&lt;/p>
&lt;/header>
</pre>

### Merged heading and subtitle

When the subtitle is contained within the same heading element as the
title, identify it in a span with the role of doc-subtitle.
<pre>
&lt;section role="doc-chapter">
&lt;h1>ORIGIN OF THE WORLD.---FIRST DYNASTY.
&lt;span role="doc-subtitle">URANUS AND GÆA. (Cœlus and Terra.)&lt;/span>
&lt;/h1>
</pre>

Tables
------

Tag tables as per the table structure. If any of the tables exceeding
more than 5 columns are captured as image to accommodate the device
restriction \[Insert Cross-reference for Image treatment of tables\],
then the table should be coded with proper table tagging and referred to
the particular table image through aria-label attribute. This will help
the screen reader users to perceive the full table information as an
alternative to the image.

Tables that have a title should use the *caption* element. Headers
should be contained within a *thead* element and footers within a
*tfoot* element. The rows that represent the body of the table should be
contained within a *tbody* element.

### Irregular header 

The following table has headers that span columns and rows:

<table border="1">
<thead>
<tr>
<th id="ship" scope="colgroup" colspan="2">Shipping.</th>
<th id="stock" scope="colgroup" rowspan="2">Stock.</th>
<th id="wages" scope="colgroup" colspan="2">Wages.</th>
<th id="wt" scope="colgroup" colspan="2">Weights.</th>
<th id="name" scope="colgroup" rowspan="2">Name of Colony.</th>
</tr>
<tr>
<th scope="col">Book, page.</th>
<th scope="col">Appx, page.</th>
<th scope="col">Book, page.</th>
<th scope="col">Appx, page.</th>
<th scope="col">Book, page.</th>
<th scope="col">Appx, page.</th>
</tr>
</thead>
<tbody>
<tr>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

To make these headings accessible, use colgroup elements with the scope
attribute:

<pre>
&lt;table border="1">
&lt;colgroup span="2"/>
&lt;colgroup span="1"/>
&lt;colgroup span="2"/>
&lt;colgroup span="2"/>
&lt;colgroup span="1"/>
&lt;thead>
&lt;tr>
&lt;th id="ship" colspan="2" scope="colgroup">Shipping.&lt;/th>
&lt;th id="stock" rowspan="2" scope="colgroup">Stock.&lt;/th>
&lt;th id="wages" colspan="2" scope="colgroup">Wages.&lt;/th>
&lt;th id="wt" colspan="2" scope="colgroup">Weights.&lt;/th>
&lt;th id="name" rowspan="2" scope="colgroup">Name of Colony.&lt;/th>
&lt;/tr>
&lt;tr>
&lt;th scope="col">Book, page.&lt;/th>
&lt;th scope="col">Appx, page.&lt;/th>
&lt;th scope="col">Book, page.&lt;/th>
&lt;th scope="col">Appx, page.&lt;/th>
&lt;th scope="col">Book, page.&lt;/th>
&lt;th scope="col">Appx, page.&lt;/th>
&lt;/tr>
&lt;/thead>
&lt;tbody>
...
&lt;/tbody>
&lt;/table>
</pre>

### Complex headings 

The following table shows a distance chart with the start destinations
defined in the first row and at the end destination at the end of each
subsequent row:

<table border="1">
<thead>
<tr>
<th scope="col">Vancouver</th>
<th scope="col">Calgary</th>
<th scope="col">Saskaton</th>
<th scope="col">Winnipeg</th>
<th scope="col">Toronto</th>
<th scope="col">Montreal</th>
<th scope="col">St. John's</th>
<td></td>
</tr>
</thead>
<tbody>
<tr>
<td class="center">7323</td>
<td class="center">6334</td>
<td class="center">5838</td>
<td class="center">5010</td>
<td class="center">3141</td>
<td class="center">2602</td>
<td class="center"></td>
<th scope="row">St. John's</th>
</tr>
<tr>
<td class="center">4271</td>
<td class="center">3743</td>
<td class="center">3232</td>
<td class="center">2408</td>
<td class="center">539</td>
<td class="center"></td>
<td class="center">2602</td>
<th scope="row">Montreal</th>
</tr>
</tbody>
</table>

Use scope=\"col\" to make the start destinations the column headers and
scope=\"row\" to make the end destinations the row headers:

<pre>
&lt;table border="1">
&lt;thead>
&lt;tr>
&lt;th scope="col">Vancouver&lt;/th>
&lt;th scope="col">Calgary&lt;/th>
&lt;th scope="col">Saskaton&lt;/th>
&lt;th scope="col">Winnipeg&lt;/th>
&lt;th scope="col">Toronto&lt;/th>
&lt;th scope="col">Montreal&lt;/th>
&lt;th scope="col">St. John's&lt;/th>
&lt;td>&lt;/td>
&lt;/tr>
&lt;/thead>
&lt;tbody>
&lt;tr>
&lt;td class="center">7323&lt;/td>
&lt;td class="center">6334&lt;/td>
&lt;td class="center">5838&lt;/td>
&lt;td class="center">5010&lt;/td>
&lt;td class="center">3141&lt;/td>
&lt;td class="center">2602&lt;/td>
&lt;td class="center">&lt;/td>
&lt;th scope="row">St. John's&lt;/th>
&lt;/tr>
&lt;tr>
&lt;td class="center">4271&lt;/td>
&lt;td class="center">3743&lt;/td>
&lt;td class="center">3232&lt;/td>
&lt;td class="center">2408&lt;/td>
&lt;td class="center">539&lt;/td>
&lt;td class="center">&lt;/td>
&lt;td class="center">2602&lt;/td>
&lt;th scope="row">Montreal&lt;/th>
&lt;/tr>
&lt;/tbody>
&lt;/table>
</pre>

### Layered headings 

The following table combines headers from the top of each column and
beginning of each row:

<table border="1">
<caption>Table IX.4 Income Distribution Among Families 1929-1997</caption>
<thead>
<tr>
<th id="t4-pct">% Families</th>
<th id="t4-1929" colspan="2">1929</th>
<th id="t4-1970" colspan="2">1970</th>
<th id="t4-1997" colspan="2">1997</th>
</tr>
</thead>
<tbody>
<tr>
<th id="t4-low20">Lowest 20%</th>
<td headers="t4-1929 t4-low20">3.5%</td>
<td headers="t4-1929 t4-low20">3.5%</td>
<td headers="t4-1970 t4-low20">5.5%</td>
<td headers="t4-1970 t4-low20">5.5%</td>
<td headers="t4-1997 t4-low20">4.2%</td>
<td headers="t4-1997 t4-low20">4.2%</td>
</tr>
</tbody>
</table>

The headers attribute is used to provide the IDs of the cells that
contain the relevant heading text:

<pre>
&lt;table border="1">
&lt;caption>Table IX.4 Income Distribution Among Families 1929-1997&lt;/caption>
&lt;thead>
&lt;tr>
&lt;th id="t4-pct">% Families&lt;/th>
&lt;th id="t4-1929" colspan="2">1929&lt;/th>
&lt;th id="t4-1970" colspan="2">1970&lt;/th>
&lt;th id="t4-1997" colspan="2">1997&lt;/th>
&lt;/tr>
&lt;/thead>
&lt;tbody>
&lt;tr>
&lt;th id="t4-low20">Lowest 20%&lt;/th>
&lt;td headers="t4-1929 t4-low20">3.5%&lt;/td>
&lt;td headers="t4-1929 t4-low20">3.5%&lt;/td>
&lt;td headers="t4-1970 t4-low20">5.5%&lt;/td>
&lt;td headers="t4-1970 t4-low20">5.5%&lt;/td>
&lt;td headers="t4-1997 t4-low20">4.2%&lt;/td>
&lt;td headers="t4-1997 t4-low20">4.2%&lt;/td>
&lt;/tr>
&lt;/tbody>
&lt;/table>
</pre>

## Lists

Tag list items with proper list tags. Do not use other elements such as
\<p\>. By tagging the list items with proper list elements, the screen
reader users can perceive meaningful information and will know that they
are reading list items.

### Unordered list 

<pre>
&lt;ul>
&lt;li>Credit, consumer, 164&lt;/li>
&lt;li>Cross-functional contact, 10-11&lt;/li>
&lt;li>Culture
&lt;ul>
&lt;li>buyer behavior and, 85&lt;/li>
&lt;li>defined, 85, 98, 118&lt;/li>
...
&lt;/ul>
&lt;/li>
...
&lt;/ul>
</pre>

Excerpt from: Core Concepts of Marketing --- John Burnett

### Definition list 

Definition list tagging is required for Apex EPUB deliveries, but
considered optional for third-party partners to University of Michigan.

<pre>
&lt;dl>
&lt;dt>&lt;def>Exchange function&lt;/def>&lt;/dt>
&lt;dd>
Sales of the product to the various members
of the channel of distribution.
&lt;/dd>
&lt;dt>&lt;def>Physical distribution function&lt;/def>&lt;/dt>
&lt;dd>
Moves the product through the exchange
channel, along with title and ownership.
&lt;/dd>
&lt;dt>&lt;def>Marketing channel&lt;/def>&lt;/dt>
&lt;dd>
Sets of independent organizations involved
in the process of making a product or
service available for use or consumption
as well as providing a payment mechanism
for the provider.
&lt;/dd>
...
&lt;/dl>
</pre>

Excerpt from: Core Concepts of Marketing --- John Burnett

## Links

The recommended best practice is to include links as meaningful text if
the surrounding text is inadequate to define the purpose of the link. By
providing meaningful text interpretation, the screen reader user can
understand the purpose of the link and decide if they need to navigate
to that particular link.

### Links spec

All the cross-references such as table of contents, notes and
footnotes are two-way linked. Other references such as page, section,
figure, etc., are one-way linked. The web address and email address
links are active.

### Link with full context of destination

The user can determine the destination of the link from the text of
the \<a\> element alone.

<pre>
&lt;p>For more information, refer to &lt;a href="#...">Section 1.1 of Web Publications&lt;/a>&lt;/p>
</pre>

### Link with alternate text

Adding alternate text is an optional best practice if neither of the
above conditions are met. Use the title attribute to provide
additional context.

<pre>
&lt;a href="#..." title="The EPUB specifications">click here&lt;/a>
</pre>

### Visual distinctive linking

**Bold Text Option:** By specifying bolder, either a medium font or a
bold one will make links visually stand out from their surrounding
text.

<pre>
a {
    text-decoration: none;
    font-weight: bolder;
    color: rgb(51,102,204);
  }
</pre>

**Dotted Border Option:** A dotted border is placed under all links to
highlight them instead of a line.

<pre>
a {
    text-decoration: none;
    padding-bottom: 0.3rem;
    border-bottom: 0.1rem dotted rgb(100,100,100);
  }
</pre>

## Images

The images should have an alternate text for the screen reader users. By
providing an alternate text for non-visual content, the screen reader
users can perceive information about the image through the alternate
text provided by us.

### Significant simple image (no description required) 

<pre>
&lt;img src="covers/9781449328030_lrg.jpg"
     alt="Accessible EPUB 3 - First Edition"/>
</pre>

### Extended description via hyperlink

Extended description inclusion and linking via a hyperlink are
optional unless provided in the source.
>
The following example uses simple hyperlinks to link to a note at the
end of the chapter.

The descriptions could also be located in a separate file, but this
might have a performance impact for users (i.e., it will require the
reading system to unload and reload each document each time the user
follows a link).

An image could also be used to minimize the appearance of the link,
but some reading systems have issues with such links.

<pre>
&lt;figure id="fig-01">
&lt;img src="graphics/water-cycle.jpg" 
    alt="The hydrologic cycle, showing the
    circular nature of the process as water
    evaporates from a body of water and
    eventually returns to it"/>
&lt;figcaption>
The hydrologic cycle. &lt;a role="doc-noteref" href="#desc-01">Description&lt;/a>
&lt;/figcaption>
&lt;/figure>
...
&lt;h2>Image Descriptions&lt;/h2>
&lt;aside role="doc-footnote" id="desc-01">
&lt;p>
&lt;a role="doc-backlink" href="#fig-01">Figure 1.&lt;/a>
 --- The diagram shows
the processes of evaporation, condensation,
evapotranspiration, water storage in ice and snow, and
precipitation. A large body of water ...
&lt;/p>
&lt;/aside>
</pre>

### Decorative image

An empty alt attribute is complimented by the role presentation to
indicate that the image contains no information for users.
<pre>
&lt;img src="graphics/gothic-border.png" role="presentation" alt=""/>
</pre>

## Code Blocks

Representations of computer code within the text, referred to here as
code blocks should be encoded semantically when possible. Never use an
image to represent lines of code, inline code, or code blocks.

### Inline Code

Code to be displayed inline with paragraph text should be indicated with
its equivalent semantic element.
<pre>
&lt;p>In table 2.2, the FizzBuzz algorithm ... is described as a
&lt;i>loop&lt;/i> because it continues to compute results so long as the
proper conditions are met, in this case while the input amount
(&lt;code>i&lt;/code>) is a number lower than or equal to 100.
Example 2.2.a, on the left, frames its computation in an initial
"catch-all" condition statement, that is, that &lt;code>i&lt;/code>
is a multiple of three &lt;i>or&lt;/i> of five. (The syntax
&lt;code>i%3&lt;/code> checks whether "&lt;code>i&lt;/code> divided by 3"
has a remainder of zero.) Then it checks each of those subconditions
independently of one another. This means that &lt;code>i&lt;/code> ...
&lt;/p>
</pre>

### Code Blocks

Code that needs its formatting preserved and should display as a block
of text, like a blockquote, should be identified a figure and be wrapped
with elements to preserve formatting of the code. Note the application
of the CSS class code on the figure element. Rules defined in the
associate spec CSS file help ensure formatting is preserved and line
breaks occur when lines of code are excessively long.
<pre>
&lt;figure class="code">
&lt;pre>
&lt;code>
if invariance &#x3e; the random of engineering
        and not categorical then
    put ideals + one into media
    if subversive then
        put false into subversive
    end if

    if media &#x3e; instantiation then
        put one into media
    end if
end if
&lt;/code>
&lt;/pre>
&lt;figcaption>
&lt;span id="p51" class="page" epub:type="pagebreak" role="doc-pagebreak" aria-label="51">Page 51 &#8594;&lt;/span>
&lt;p class="bqt">(Cayley 2002)&lt;/p>
&lt;/figcaption>
&lt;/figure>
</pre>

### Code Blocks with Line Numbers

There may be instances where code blocks are long or an author refers to
specific lines of code in the surrounding text. There also may be a
desire to allow readers to copy and paste code blocks without line
numbers included in the copied text. To do so one will need to divert
from semantic encoding, and use CSS-only to include line numbers. Apply
a CSS attribute which utilizes CSS line counting to provide line numbers
automatically.
<pre>
&lt;figure class="code-linenumbers">
&lt;figcaption>
&lt;a data-locator="p157" class="page">&lt;/a>Practice Script 5.3: Revised simple statement combination
&lt;/figcaption>
&lt;pre>
&lt;span>myVariable = true;&lt;/span>
&lt;span>if (myVariable == true) {&lt;/span>
&lt;span> "The value of myVariable is TRUE";&lt;/span>
&lt;span>} else {&lt;/span>
&lt;span> "The value of myVariable is FALSE";&lt;/span>
&lt;span>}&lt;/span>
&lt;/pre>
&lt;/figure>
</pre>

### Code Blocks with Line Numbers as Tables

In cases where code does not need to be copied and pasted but the
display of line numbers is desirable, it is acceptable to encode the
block of code as a table. For historical references to code this may be
the most desirable, where excerpts of code are only needed to be
displayed and line numbers start not a 1, but 3977, for example.
<pre>
&lt;table class="code">
&lt;thead>
&lt;tr>
&lt;th class="th" colspan="2">&lt;a data-locator="p10"
class="page">&lt;/a>Table 1.1. Excerpt from Heartbleed patch
(t1\_lib.c) by snhenson et al. (2015)&lt;/th>
&lt;/tr>
&lt;tr>
&lt;th class="tch">Line&lt;/th>
&lt;th class="tch">Code&lt;/th>
&lt;/tr>
&lt;/thead>
&lt;tbody>
&lt;tr>
&lt;td>
&lt;pre>&lt;code>3977&lt;/code>&lt;/pre>
&lt;/td>
&lt;td>
&lt;pre>
&lt;code>/* Read type and payload length first */&lt;/code>
&lt;/pre>
&lt;/td>
&lt;/tr>
&lt;tr>
&lt;td>
&lt;pre>&lt;code>3978&lt;/code>&lt;/pre>
&lt;/td>
&lt;td>
&lt;pre>
&lt;code>if (1 + 2 + 16 &#x3e; s-&#x3e;s3-&#x3e;rrec.length)&lt;/code>
&lt;/pre>
&lt;/td>
&lt;/tr>
&lt;/tbody>
&lt;/table>
</pre>

### Comparing Code Blocks with Line Numbers

In other cases, two different blocks of code may need to be compared to
one another side-by-side, along with the display of line numbers. In
this case the code blocks should be encoded in a table, and follow the
general pattern in 1.16.4. Note that in this case an additional CSS
attribute is applied to the table element.
<pre>
&lt;table class="code compare">
&lt;thead>
&lt;tr>
&lt;th class="th" colspan="3">&lt;a data-locator="p59"
class="page">&lt;/a>Table 2.3. Two example FizzBuzz loops in
Ruby&lt;/th>
&lt;/tr>
&lt;tr>
&lt;th class="tch" style="width: 10%;">Line&lt;/th>
&lt;th class="tch">Example 2.3.a&lt;/th>
&lt;th class="tch">Example 2.3.b&lt;/th>
&lt;/tr>
&lt;/thead>
&lt;tbody>
&lt;tr>
&lt;td>
&lt;pre>&lt;code>1&lt;/code>&lt;/pre>
&lt;/td>
&lt;td>
&lt;pre>
&lt;code>for i in 1..100&lt;/code>
&lt;/pre>
&lt;/td>
&lt;td>
&lt;pre>
&lt;code>100.times do |i|&lt;/code>
&lt;/pre>
&lt;/td>
&lt;/tr>
&lt;tr>
&lt;td>
&lt;pre>&lt;code>2&lt;/code>&lt;/pre>
&lt;/td>
&lt;td>
&lt;pre>
&lt;code> if i%3 == 0 then&lt;/code>
&lt;/pre>
&lt;/td>
&lt;td>
&lt;pre>
&lt;code> i = i+1&lt;/code>
&lt;/pre>
&lt;/td>
&lt;/tr>
&lt;/tbody>
&lt;/table>
</pre>

Footnotes and Endnotes
----------------------

In general, the footnotes and endnotes are highly recommended to place
at logical break of the book such as end of the chapter or end of the
book, which will help the screen reader users to read the primary text.
Also, the two-way link provided for the footnotes and endnotes reference
numbers in between the primary text will help the screen reader users to
navigate if they require.

Footnote and endnote tagging per the following examples is required for
Apex EPUB deliveries, but considered optional for third-party partners
to University of Michigan.

### Footnotes in the body 
<pre>
&lt;p>
In that year&lt;a href="\#ft2f" epub:type="noteref">2&lt;/a>
there were 67 mills engaged in the manufacture of cotton goods ...
&lt;/p>
&lt;aside id="ft2f" epub:type="footnote">
&lt;p>
2 The manufacturing statistics for 1900 which
follow are not those given in the Twelfth
Census, but are taken from the
&lt;em>Census of Manufactures&lt;/em> ...
&lt;/p>
&lt;/aside>
&lt;p>...&lt;/p>
</pre>

### Endnote section 

The HTML Model allows for lists to contain headings, paras, images,
tables, etc. This means that applying list tagging can accommodate
Endnote structures following \<ol\>.

If it is necessary to match the presentation of the text for editorial
reasons, then it is suggested to use an unordered list tagging so that
each endnote item is encapsulated as a list item.

A cluster of paras with \<p class="xxxxx"\> tagging does not afford the
same flexibility as list encoding, nor provide precision for isolating
start and end of notes.
<pre>
&lt;section epub:type="endnotes">
&lt;h2>End Notes&lt;/h2>
&lt;ol>
&lt;li id="en001" epub:type="endnote">
According to the usual nomenclature, the
branch flowing S.W. is called the Chattooga;
this unites with the Tallulah to form the
Tugaloo, which ...
&lt;/li>
...
&lt;/ol>
&lt;/section>
</pre>

### Back-linking notes 
<pre>
&lt;li id="en001" epub:type="endnote">
&lt;a href="\#en01-ref" title="note reference 1">1&lt;/a>
According to the usual nomenclature, the ...
&lt;/li>
</pre>

## Content Numbering

### Page Break Numbering

Page numbers should follow the EPUB3 Accessibility Guidelines.
<https://idpf.github.io/a11y-guidelines/content/xhtml/pagenum.html>

**Example coding:**
<pre>
&lt;span id="p1" class="page" epub:type="pagebreak"
      role="doc-pagebreak" aria-label="1">Page 1 &\#8594;&lt;/span>
</pre>

### Paragraph Numbering

Paragraph numbering requires adding a class identifier and id value to a
\<p\>.

Note: Paragraph numbering is optional, but recommended when present in
the source document.

Example coding:

<pre>
&lt;p class="numberedpara" id="para11" title="Para11"/>
</pre>

### Line Numbering

Line numbering requires adding a class identifier and id value to a
\<p\>.

Example coding:
<pre>
&lt;p class="numberedline" id="line11" title="Line11"/>
</pre>

Chapter Split
-------------

When chapters contain a large number of images and the total file size
of the images exceeds 2 Mb, then consider splitting the chapter into a
series of html files. This will create smaller files for faster download
and rendering within the Fulcrum EPUB system. Inside each html file,
please include the yellow highlighted metadata updated by section to
represent relationships between all files for a chapter. The example
snippet below is for file chapter2a. The reason for the metadata
inclusion is to provide information so that UM is able to parse files to
allow only chapters to display.
<pre>
&lt;html xmlns="http://www.w3.org/1999/xhtml"
      xmlns:epub="http://www.idpf.org/2007/ops" xml:lang="eng">
&lt;head>
&lt;title>More&lt;/title>
&lt;link rel="stylesheet" href="../Styles/stylesheet.css" type="text/css"/>
&lt;meta name="viewport" content="initial-scale=1.0;maximum-scale=5.0"/>
&lt;meta content="chapter2" name="chapter2a" role="section"/>
&lt;/head>
&lt;body>
&lt;div>
&lt;h3 class="subhead" id="sub4">&lt;em>The Mid-Republican Period: The House&lt;/em>&lt;/h3>
</pre>

## CSS Stylesheet

### Standard CSS

If possible, use following standard CSS for EPUB3 conversion. Add unique
styles per book as needed as additional styles at the bottom of the
standard CSS.

### CSS Units

-   Font-size should always be defined in %
-   Do not use fixed values (**mm, cm, in, pt** or **pc**) in CSS file.
-   Control the **font style** over the css (avoid inline styles)
-   Create external style sheet
    - It is necessary to validate CSS (refer http://www.css-validator.org/).
    - Do not capture \<i\> (capture as \<em\>)
    - Do capture \<b\> for bold text in XHTML files

### Colors

The best practice is to avoid using color to differentiate the
information of a text. For example, if the color of a text provides a
meaning to the content, then there should be some alternate method to
convey the information to screen reader user.

### Background Images

Setting the contrast between the background colors and images will help
readers who have difficulty in distinguishing contrasts. Color contrast
of 4:5:1 is the best practice followed in the industry. Check contrast
using the following link.
[[https://webaim.org/resources/contrastchecker/]{.underline}](https://webaim.org/resources/contrastchecker/).

### Hidden Content

There should not be any hidden content available in the EPUB files.

Exception: Code long-descriptions as a separate instance in a file and
it is permissible to have it remain hidden text.

### CSS Property Reference

EPUB 3 user agents that visually render content may provide support for
the CSS properties listed below, but inclusion is optional. Properties
not listed may still be used (e.g., from evolving CSS 3 modules), but
content authors should use due diligence and assess the impact on
rendering and accessibility when using such properties.

### CSS 2.1

Table 1. Acceptable Styles

<table border="1">
<thead>
<tr>
<th>Property</th>
<th>Considerations</th>
</tr>
</thead>
<tbody>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/colors.html#propdef-background">background</a
></p></td>
<td style="vertical-align:top"><ul>
<li><p>The background property is a shorthand for defining one or
more properties. Refer to each individual background-* property for
potential issues.</p><p><u>Note</u> that background properties are
largely unsupported at this time outside of fixed layouts.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/colors.html#propdef-background-attachment"
>background-attachment</a></p></td>
<td style="vertical-align:top"></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/colors.html#propdef-background-color"
>background-color</a></p></td>
<td style="vertical-align:top"><ul>
<li><p>Ensure sufficient contrast with text color.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/colors.html#propdef-background-image"
>background-image</a></p></td>
<td style="vertical-align:top"><ul>
<li><p>Ensure sufficient contrast with content color (text and graphic).</p
></li>
<li><p>High mix of gradients and colors in images can make reading
overlaid text difficult.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/colors.html#propdef-background-position"
>background-position</a></p></td>
<td style="vertical-align:top"></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/colors.html#propdef-background-repeat"
>background-repeat</a></p></td>
<td style="vertical-align:top"></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/box.html#propdef-border">border</a
></p><p><a href="http://www.w3.org/TR/CSS21/box.html#propdef-border-top"
>border-top</a></p><p><a
href="http://www.w3.org/TR/CSS21/box.html#propdef-border-right">border-right</a
></p><p><a
href="http://www.w3.org/TR/CSS21/box.html#propdef-border-bottom">border-bottom</a
></p><p><a
href="http://www.w3.org/TR/CSS21/box.html#propdef-border-left">border-left</a
></p></td>
<td style="vertical-align:top"><ul>
<li><p>These border properties are shorthands for defining one or
more properties. Refer to each individual border-* property for issues.</p
></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/tables.html#propdef-border-collapse"
>border-collapse</a></p></td>
<td style="vertical-align:top"></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/box.html#propdef-border-color">border-color</a
></p><p><a
href="http://www.w3.org/TR/CSS21/box.html#propdef-border-top-color"
>border-top-color</a></p><p><a
href="http://www.w3.org/TR/CSS21/box.html#propdef-border-right-color"
>border-right-color</a></p><p><a
href="http://www.w3.org/TR/CSS21/box.html#propdef-border-bottom-color"
>border-bottom-color</a></p><p><a
href="http://www.w3.org/TR/CSS21/box.html#propdef-border-left-color"
>border-left-color</a></p></td>
<td style="vertical-align:top"><ul>
<li><p>An element's border color must never be the sole means of conveying
information about the nature of its content. See the <a
href="http://kb.daisy.org/publishing/docs/css/color.html">Color info
page</a>.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/tables.html#propdef-border-spacing"
>border-spacing</a></p></td>
<td style="vertical-align:top"></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/box.html#propdef-border-style">border-style</a
></p><p><a
href="http://www.w3.org/TR/CSS21/box.html#propdef-border-top-style"
>border-top-style</a></p><p><a
href="http://www.w3.org/TR/CSS21/box.html#propdef-border-right-style"
>border-right-style</a></p><p><a
href="http://www.w3.org/TR/CSS21/box.html#propdef-border-bottom-style"
>border-bottom-style</a></p><p><a
href="http://www.w3.org/TR/CSS21/box.html#propdef-border-left-style"
>border-left-style</a></p></td>
<td style="vertical-align:top"></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/box.html#propdef-border-width">border-width</a
></p><p><a
href="http://www.w3.org/TR/CSS21/box.html#propdef-border-top-width"
>border-top-width</a></p><p><a
href="http://www.w3.org/TR/CSS21/box.html#propdef-border-right-width"
>border-right-width</a></p><p><a
href="http://www.w3.org/TR/CSS21/box.html#propdef-border-bottom-width"
>border-bottom-width</a></p><p><a
href="http://www.w3.org/TR/CSS21/box.html#propdef-border-left-width"
>border-left-width</a></p></td>
<td style="vertical-align:top"><ul>
<li><p>When using color to convey meaning, ensure borders are thick
enough that visual users can discern the color.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/visuren.html#propdef-bottom">bottom</a
></p><p><a href="http://www.w3.org/TR/CSS21/visuren.html#propdef-left"
>left</a></p><p><a
href="http://www.w3.org/TR/CSS21/visuren.html#propdef-right">right</a
></p><p><a href="http://www.w3.org/TR/CSS21/visuren.html#propdef-top"
>top</a></p></td>
<td style="vertical-align:top"><ul>
<li><p>User agent support for absolute and fixed positioning is not
guaranteed.</p></li>
<li><p>Content should not be positioned in a way that makes its discoverability
problematic for users with low vision and/or using zooming software.</p
></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/tables.html#propdef-caption-side"
>caption-side</a></p></td>
<td style="vertical-align:top"></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/visuren.html#propdef-clear">clear</a
></p></td>
<td style="vertical-align:top"></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/colors.html#propdef-color">color</a
></p></td>
<td style="vertical-align:top"><ul>
<li><p>See the <a
href="http://kb.daisy.org/publishing/docs/css/color.html">Color info
page</a> for the range of considerations when coloring text and graphical
content.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/generate.html#propdef-counter-increment"
>counter-increment</a></p><p><a
href="http://www.w3.org/TR/CSS21/generate.html#propdef-counter-reset"
>counter-reset</a></p></td>
<td style="vertical-align:top"></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/ui.html#propdef-cursor">cursor</a
></p></td>
<td style="vertical-align:top"><ul>
<li><p>Avoid changing the cursor such that clickable elements are
no longer distinguishable.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/visuren.html#propdef-display">display</a
></p></td>
<td style="vertical-align:top"><ul>
<li><p>Setting the display property to the value none removes the
element from rendering both visually and to assistive technologies.
It is not a mechanism for hiding content from visual display that
should be rendered by ATs.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/tables.html#propdef-empty-cells"
>empty-cells</a></p></td>
<td style="vertical-align:top"><ul>
<li><p>Setting the empty-cells property is not required for HTML5
tables, as borders are rendered (do not insert placeholder text such
as dashes or non-breaking spaces).</p></li>
<li><p>For forwards compatibility with EPUB 2 user agents, the property
should be set to the value show to ensure table borders are drawn
around empty cells.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/visuren.html#propdef-float">float</a
></p></td>
<td style="vertical-align:top"><ul>
<li><p>Elements should not be floated in a way that makes their discoverability
problematic for users with low vision and/or using zooming software.</p
></li>
<li><p>Ensure sufficient margins exist around floated content so that
it is clearly distinguishable from the content that flows around it.</p
></li>
<li><p>When floating primary content to the right, ensure that it
is not positioned in the markup to accommodate the float (i.e., it
occurs at the logical reading point so that it makes sense in non-visual
playback contexts).</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/fonts.html#propdef-font">font</a
></p></td>
<td style="vertical-align:top"><ul>
<li><p>The font property is a shorthand for defining one or more properties.
Refer to each individual font-* property for issues.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/fonts.html#propdef-font-family">font-family</a
></p></td>
<td style="vertical-align:top"><ul>
<li><p>Avoid fonts that do not provide sufficient character differentiation,
such as sans-serif fonts that represent capital I, lower-case L and
the number 1 as identical (or near-identical) characters (e.g., Arial).</p
></li>
<li><p>Avoid cursive and highly ornamented fonts that can be difficult
for users to decipher.</p></li>
<li><p>Try to limit the number of fonts used in any given publication
and use families consistently (e.g., one family for headings and one
for body content).</p></li>
<li><p>Give preference to fonts that provide sufficient kerning between
characters.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/fonts.html#propdef-font-size">font-size</a
></p></td>
<td style="vertical-align:top"><ul>
<li><p>Use relative sizes such as percentages and ems to facilitate
scaling.</p></li>
<li><p>Ensure default font size does not affect legibility of the
prose (e.g., avoid specifying x-small, xx-small and equivalent font
sizes).</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/fonts.html#propdef-font-style">font-style</a
></p></td>
<td style="vertical-align:top"><ul>
<li><p>Use CSS to apply italics only for decorative purposes (similar
to using the i element). Use em tags if the words are to be stressed.</p
></li>
<li><p>Avoid lengthy use of decorative italics, as italicized words
can be harder to read than roman face.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/fonts.html#propdef-font-variant"
>font-variant</a></p></td>
<td style="vertical-align:top"></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/fonts.html#propdef-font-weight">font-weight</a
></p></td>
<td style="vertical-align:top"><ul>
<li><p>Use CSS to apply bolding only for decorative purposes (similar
to using the b element). Use strong tags if the words are to be stressed.</p
></li>
<li><p>Avoid lengthy use of decorative bolding, as bolded words can
be harder to read than roman face.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/visudet.html#propdef-height">height</a
></p></td>
<td style="vertical-align:top"><ul>
<li><p>Assistive technologies typically ignore content that has 0
height and/or width set on its containing element, so do not use this
property to hide content that is only intended for non-visual playback.</p
></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/text.html#propdef-letter-spacing"
>letter-spacing</a></p></td>
<td style="vertical-align:top"><ul>
<li><p>The letter-spacing property can be used to increase the kerning
between letters to improve the readability of tightly constructed
fonts.</p></li>
<li><p>Whitespace should never be added between the letters of a word
that is not intended to be spelled out. Always use this property to
visually expand the spacing between characters when such spacing is
necessary.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/visudet.html#propdef-line-height"
>line-height</a></p></td>
<td style="vertical-align:top"><ul>
<li><p>Use caution when changing line heights. Slight increases in
the line height can improve overall readability, but too much space
between lines can have the opposite effect (e.g., it becomes harder
to distinguish paragraphs).</p></li>
<li><p>Avoid shrinking the line height to compress content.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/generate.html#propdef-list-style"
>list-style</a></p></td>
<td style="vertical-align:top"><ul>
<li><p>The list-style property is a shorthand for defining one or
more properties. Refer to each individual list-style-* property for
issues.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/generate.html#propdef-list-style-image"
>list-style-image</a></p></td>
<td style="vertical-align:top"><ul>
<li><p>Avoid using images to convey the meaning of a list. If the
image is important to comprehension of the items, ensure that a semantic
is attached to the list to convey that meaning. If the list represents
a figure or aside, use the appropriate container element and include
a caption.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/generate.html#propdef-list-style-position"
>list-style-position</a></p></td>
<td style="vertical-align:top"></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/generate.html#propdef-list-style-type"
>list-style-type</a></p></td>
<td style="vertical-align:top"><ul>
<li><p>Do not change the nature of a list using the list-style-type
property (e.g., to not use the property to give an unordered list
the appearance of ordering).</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/visudet.html#propdef-max-height"
>max-height</a></p><p><a
href="http://www.w3.org/TR/CSS21/visudet.html#propdef-max-width">max-width</a
></p><p><a
href="http://www.w3.org/TR/CSS21/visudet.html#propdef-min-height"
>min-height</a></p><p><a
href="http://www.w3.org/TR/CSS21/visudet.html#propdef-min-width">min-width</a
></p></td>
<td style="vertical-align:top"></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/page.html#propdef-orphans">orphans</a
></p><p><a href="http://www.w3.org/TR/CSS21/page.html#propdef-widows"
>widows</a></p></td>
<td style="vertical-align:top"></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/ui.html#propdef-outline">outline</a
></p><p><a
href="http://www.w3.org/TR/CSS21/ui.html#propdef-outline-color">outline-color</a
></p><p><a
href="http://www.w3.org/TR/CSS21/ui.html#propdef-outline-style">outline-style</a
></p><p><a
href="http://www.w3.org/TR/CSS21/ui.html#propdef-outline-width">outline-width</a
></p></td>
<td style="vertical-align:top"><ul>
<li><p>Outlines surround borders and serve a similar function. The
issues with each are the same. See the corresponding border properties
for more information.</p></li>
<li><p>Ensure when using both borders and outlines that sufficient
contrast is maintained between them if they both visually convey information.</p
></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/visufx.html#propdef-overflow">overflow</a
></p></td>
<td style="vertical-align:top"><ul>
<li><p>Avoid using the hidden value, as content may not be visible,
especially when zoomed.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/box.html#propdef-padding">padding</a
></p><p><a
href="http://www.w3.org/TR/CSS21/box.html#propdef-padding-top">padding-top</a
></p><p><a
href="http://www.w3.org/TR/CSS21/box.html#propdef-padding-right">padding-right</a
></p><p><a
href="http://www.w3.org/TR/CSS21/box.html#propdef-padding-bottom"
>padding-bottom</a></p><p><a
href="http://www.w3.org/TR/CSS21/box.html#propdef-padding-left">padding-left</a
></p></td>
<td style="vertical-align:top"></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/page.html#propdef-page-break-after"
>page-break-after</a></p><p><a
href="http://www.w3.org/TR/CSS21/page.html#propdef-page-break-before"
>page-break-before</a></p><p><a
href="http://www.w3.org/TR/CSS21/page.html#propdef-page-break-inside"
>page-break-inside</a></p></td>
<td style="vertical-align:top"></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/visuren.html#propdef-position">position</a
></p></td>
<td style="vertical-align:top"><ul>
<li><p>Absolute positioning should not be used to re-order content
differently than it is laid out in the markup.</p></li>
<li><p>Elements should not be absolutely positioned in a way that
makes their discoverability problematic for users with low vision
and/or using zooming software.</p></li>
<li><p>Note that the fixed value is not included in the EPUB 3 Style
Sheets profile and its use is not recommended (see the <a
href="http://idpf.org/epub3/latest/contentdocs#sec-css-oeb-head-foot"
>oeb-page-head and oeb-page-foot</a> custom properties for including
static headers and footers).</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/generate.html#propdef-quotes">quotes</a
></p></td>
<td style="vertical-align:top"></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/tables.html#propdef-table-layout"
>table-layout</a></p></td>
<td style="vertical-align:top"></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/text.html#propdef-text-align">text-align</a
></p></td>
<td style="vertical-align:top"><ul>
<li><p>Avoid justifying text, as the uneven spacing that occurs between
words can reduce the readability for some people.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/text.html#propdef-text-decoration"
>text-decoration</a></p></td>
<td style="vertical-align:top"><ul>
<li><p>Use the del element to semantically mark deleted text.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/text.html#propdef-text-indent">text-indent</a
></p></td>
<td style="vertical-align:top"><ul>
<li><p>A sometimes used trick to hide text for assistive technologies
is to use a large negative value, but like negative margins this technique
is not reliable in user agents and may cause issues depending on the
user's preferred text direction.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/text.html#propdef-text-transform"
>text-transform</a></p></td>
<td style="vertical-align:top"><ul>
<li><p>Avoid lengthy decorative use of capitalization as it can make
words difficult to distinguish and read.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/visudet.html#propdef-vertical-align"
>vertical-align</a></p></td>
<td style="vertical-align:top"></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/text.html#propdef-white-space">white-space</a
></p></td>
<td style="vertical-align:top"></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/visudet.html#propdef-width">width</a
></p></td>
<td style="vertical-align:top"><ul>
<li><p>Assistive technologies typically ignore content that has 0
width and/or height set on its containing element, so do not use this
property to hide content that is only intended for non-visual playback.</p
></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/text.html#propdef-word-spacing">word-spacing</a
></p></td>
<td style="vertical-align:top"><ul>
<li><p>Increasing word spacing can help improve readability of tightly
constructed fonts.</p></li>
<li><p>Use this property in preference to adding non-breaking spaces
to increase the space between words.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/visuren.html#propdef-z-index">z-index</a
></p></td>
<td style="vertical-align:top"></td>
</tr>
</tbody>
</table>

Table 2. Not Recommended Classes

<table border="1">
<thead>
<tr>
<th>Property</th>
<th>Considerations</th>
</tr>
</thead>
<tbody>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/visufx.html#propdef-clip">clip</a
></p></td>
<td style="vertical-align:top"><ul>
<li><p>Although clipping content to 1 pixel is sometimes used on the
Web to hide content, support for the property and its reliance on
absolute positioning makes the practice not recommended in EPUBs.</p
></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/generate.html#propdef-content">content</a
></p></td>
<td style="vertical-align:top"><ul>
<li><p>Any content inserted using this property should be purely presentational,
as it typically won't be available to assistive technologies.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p>direction</p></td>
<td style="vertical-align:top"><ul>
<li><p>The direction property is not supported in EPUB 3. HTML5 markup,
such as the <a
href="http://www.w3.org/TR/html/text-level -semantics.html#the-bdi-element"
>bdi</a> and <a
href="http://www.w3.org/TR/html/text-level -semantics.html#the-bdo-element"
>bdo</a> elements and <a
href="http://www.w3.org/TR/html/dom.html#the-dir-attribute">dir</a
> attribute, should be used to express directionality.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/box.html#propdef-margin">margin</a
></p><p><a href="http://www.w3.org/TR/CSS21/box.html#propdef-margin-top"
>margin-top</a></p><p><a
href="http://www.w3.org/TR/CSS21/box.html#propdef-margin-right">margin-right</a
></p><p><a
href="http://www.w3.org/TR/CSS21/box.html#propdef-margin-bottom">margin-bottom</a
></p><p><a
href="http://www.w3.org/TR/CSS21/box.html#propdef-margin-left">margin-left</a
></p></td>
<td style="vertical-align:top"><ul>
<li><p>Note that user agents typically restrict the ability to modify
body margins.</p></li>
<li><p>Changing margins to move content off screen, common on the
Web, is not guaranteed to work in user agents. This practice is also
known to cause problems depending on the user's preferred reading
direction and the placement of the content so is not recommended for
that reason, as well.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/visufx.html#propdef-visibility">visibility</a
></p></td>
<td style="vertical-align:top"><ul>
<li><p>Hidden content is not available to assistive technologies,
so do not use this property to hide content from visual rendering
that is intended to be read out.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p>azimuth</p><p>cue</p><p>cue-after</p
><p>cue-before</p><p>elevation</p><p>pause</p><p>pause-after</p><p
>pause-before</p><p>pitch</p><p>pitch-range</p><p>play-during</p><p
>richness</p><p>speak</p><p>speak-header</p><p>speak-numeral</p><p
>speak-punctuation</p><p>speech-rate</p><p>stress</p><p>voice-family</p
><p>volume</p></td>
<td style="vertical-align:top"><ul>
<li><p>Properties from the <a
href="http://www.w3.org/TR/CSS21/aural.html">CSS 2.1 Aural style sheets
informative  appendix</a> should not be used in EPUB 3. The 'aural'
media type was deprecated by the same appendix, and the <a
href="http://kb.daisy.org/publishing/docs/css/reference.html#css3speech"
>CSS 3 Speech module</a> defines the properties for the new 'speech'
type.</p></li>
</ul></td>
</tr>
</tbody>
</table>

### CSS 2.1 Pseudo-Classes

<table border="1">
<thead>
<tr>
<th>Property</th>
<th>Considerations</th>
</tr>
</thead>
<tbody>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/selector.html#dynamic-pseudo-classes"
>:active</a></p></td>
<td style="vertical-align:top"></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/selector.html#first-child">:first-child</a
></p></td>
<td style="vertical-align:top"></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/selector.html#dynamic-pseudo-classes"
>:focus</a></p></td>
<td style="vertical-align:top"></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/selector.html#dynamic-pseudo-classes"
>:hover</a></p></td>
<td style="vertical-align:top"><p>The :hover pseudo-selector should
never be used, as it is not device independent and may not be activatable
by many users as ebook users typically do not have mice.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/selector.html#lang">:lang</a></p
></td>
<td style="vertical-align:top"></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/selector.html#link-pseudo-classes"
>:link</a></p></td>
<td style="vertical-align:top"></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/selector.html#link-pseudo-classes"
>:visited</a></p></td>
<td style="vertical-align:top"></td>
</tr>
<tr>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### CSS 2.1 Pseudo-Elements

<table border="1">
<thead>
<tr>
<th>Pseudo-Element</th>
<th>Considerations</th>
</tr>
</thead>
<tbody>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/selector.html#before-and-after">:before</a
></p><p>and</p><p><a
href="http://www.w3.org/TR/CSS21/selector.html#before-and-after">:after</a
></p></td>
<td style="vertical-align:top"><ul>
<li><p>Not all assistive technologies announce text injected using
the :before and :after pseudo-elements.</p></li>
<li><p>Since the expected behavior is to announce the injected text,
avoid the using the pseudo-elements for decorative purposes.</p></li>
<li><p>Users without CSS support will not have access to the injected
text.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/selector.html#first-letter">:first-letter</a
></p></td>
<td style="vertical-align:top"></td>
</tr>
<tr>
<td style="vertical-align:top"><p><a
href="http://www.w3.org/TR/CSS21/selector.html#first-line-pseudo"
>:first-line</a></p></td>
<td style="vertical-align:top"></td>
</tr>
</tbody>
</table>

 Images
------

### Image File Types

Acceptable file types include JPG, PNG and SVG (as per EPUB3
guidelines).

### Recommended Criteria

<table border="1">
<tbody>
<tr>
<td style="vertical-align:top"><p>Resolution</p></td>
<td style="vertical-align:top"><p>Minimum 72 dpi</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>Compression</p></td>
<td style="vertical-align:top"><p>JPG Medium</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>Color space</p></td>
<td style="vertical-align:top"><p>24-bit color (RGB) or Grayscale</p
></td>
</tr>
<tr>
<td style="vertical-align:top"><p>Format</p></td>
<td style="vertical-align:top"><p>JPG for grayscale and color pictures
and photographs.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>Reading orientation</p></td>
<td style="vertical-align:top"><p>Position per reading order. Rotated
landscape images in print versions are rotated for presentation in
the EPUB.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>Size</p></td>
<td style="vertical-align:top"><p>Reference Standard CSS</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>Presentation</p></td>
<td style="vertical-align:top"><p>Maximum File Size should not exceed
1 Mb. Reprocess images greater than 1Mb in size by applying higher
compression (not to exceed JPG Medium) or resampling to reduce the
DPI.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>Exception note</p></td>
<td style="vertical-align:top"><ol>
<li><p>If a file is less than 1Mb and jpg, use jpg as is.</p></li>
<li><p>If a file is equal to or greater than 1Mb in size apply the
following treatment in Photoshop CC</p><ol>
<li><p>Image Size > Adjust dpi to 96 dpi with Resample set to Bicubic
Sharper (Reduction).</p></li>
<li><p>Save As JPEG, Quality Setting to 8 (High), Optimized.</p></li>
<li><p>The above can be batch processed.</p></li>
</ol></li>
</ol></td>
</tr>
</tbody>
</table>

**Note**: For EPUB source files, retain the images as per the source
EPUB file with the aforementioned properties.

### Cover Image

<table>
<tbody>
<tr>
<td style="vertical-align:top"><p><b>1.21.3.1</b></p></td>
<td style="vertical-align:top"><p>The cover must consist of an XHTML
file containing nothing but an image. The image must be styled to
take up the entire height of the screen. This can be achieved using
the CSS below (just an example) or follow sample CSS if available:</p
><pre>img.cover {
    height: 100%;
}</pre></td>
</tr>
<tr>
<td style="vertical-align:top"><p><b>1.21.3.2</b></p></td>
<td style="vertical-align:top"><p>Declare the cover in metadata (OPF)
(mandatory).</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p><b>1.21.3.3</b></p></td>
<td style="vertical-align:top"><p>Capture cover related metadata as
follows in .opf file:</p><pre>&lt;meta name="cover" content="cover-image" />
&lt;item id="cover-image" href="images/cover.jpg" media-type="image/jpeg"/></pre
></td>
</tr>
<tr>
<td style="vertical-align:top"><p><b>1.21.3.4</b></p></td>
<td style="vertical-align:top"><p>Minimum width of the cover should
be more than 600 px and minimum height of the cover should be 800
px captured proportionately.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p><b>1.21.3.5</b></p></td>
<td style="vertical-align:top"><p>If the cover size of the source
EPUB file is too small, then retain the cover per the source EPUB
cover. Do not increase the size of the source EPUB cover.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p><b>1.21.3.6</b></p></td>
<td style="vertical-align:top"><p>The cover image needs to fit the
page when viewed in Readium ereader to cover as much white space as
possible.</p></td>
</tr>
</tbody>
</table>

### Image/Graphic Placement

For any object rendered as an image/graphic that occurs in the midst
of a paragraph and interrupts text, it shall be placed either at the
end of the preceding paragraph or the beginning of the nearest
following paragraph within the specific page. Final placement of the
image is dependent on the closest paragraph's proximity. The image
must stay within the page marker it occurs on in the source PDF. If an
image interrupts text, and no paragraph tag that starts or ends on the
same page, then keep the image in its original location.

## Fonts

If the input EPUB file contains fonts, then retain them in the output
EPUB3 files. For web-ready PDF input files, do not embed fonts, unless
otherwise requested by customer.

## Formatting

Retain as much as possible of the formatting of the source EPUB and PDF
files in the output EPUB3 file.

## Boxed Text

Treat as text + images in reading order.

## Marginalia and Sidebars

Treat as text + images in reading order.

## Reading Order

Retain the reading order of the EPUB source files in the EPUB3 output.
For the PDF source files, then match the source reading order in the
EPUB3 output.

## DPUB ARIA Semantics

Apply DPUB ARIA semantic attributes according to the type of content.
Refer the link for code samples: <https://www.w3.org/TR/dpub-aria-1.0/>

<table border="1">
<tbody>
<tr>
<td style="vertical-align:top"><p>doc-acknowledgments</p></td>
<td style="vertical-align:top"><p>A section or statement that acknowledges
significant contributions by persons, organizations, governments and
other entities to the realization of the work.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-afterword</p></td>
<td style="vertical-align:top"><p>A closing statement from the author
or a person of importance, typically providing insight into how the
content came to be written, its significance, or related events that
have transpired since its timeline.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-appendix</p></td>
<td style="vertical-align:top"><p>A section of supplemental information
located after the primary content that informs the content but is
not central to it.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-backlink</p></td>
<td style="vertical-align:top"><p>A link that allows the user to return
to a related location in the content (e.g., from a footnote to its
reference or from a glossary definition to where a term is used).</p
></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-biblioentry</p></td>
<td style="vertical-align:top"><p>A single reference to an external
source in a bibliography. A biblioentry typically provides more detailed
information than its reference(s) in the content (e.g., full title,
author(s), publisher, publication date, etc.).</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-bibliography</p></td>
<td style="vertical-align:top"><p>A list of external references cited
in the work, which may be to print or digital sources.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-biblioref</p></td>
<td style="vertical-align:top"><p>A reference to a bibliography entry.</p
></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-chapter</p></td>
<td style="vertical-align:top"><p>A major thematic section of content
in a work.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-colophon</p></td>
<td style="vertical-align:top"><p>A short section of production notes
particular to the edition (e.g., describing the typeface used), often
located at the end of a work.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-conclusion</p></td>
<td style="vertical-align:top"><p>A concluding section or statement
that summarizes the work or wraps up the narrative.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-cover</p></td>
<td style="vertical-align:top"><p>An image that sets the mood or tone
for the work and typically includes the title and author.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-credit</p></td>
<td style="vertical-align:top"><p>An acknowledgment of the source
of integrated content from third-party sources, such as photos. Typically
identifies the creator, copyright and any restrictions on reuse.</p
></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-credits</p></td>
<td style="vertical-align:top"><p>A collection of credits.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-dedication</p></td>
<td style="vertical-align:top"><p>An inscription at the front of the
work, typically addressed in tribute to one or more persons close
to the author.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-endnote</p></td>
<td style="vertical-align:top"><p>One of a collection of notes that
occur at the end of a work, or a section within it, that provides
additional context to a referenced passage of text.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-endnotes</p></td>
<td style="vertical-align:top"><p>A collection of notes at the end
of a work or a section within it.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-epigraph</p></td>
<td style="vertical-align:top"><p>A quotation set at the start of
the work or a section that establishes the theme or sets the mood.</p
></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-epilogue</p></td>
<td style="vertical-align:top"><p>A concluding section of narrative
that wraps up or comments on the actions and events of the work, typically
from a future perspective.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-errata</p></td>
<td style="vertical-align:top"><p>A set of corrections discovered
after initial publication of the work, sometimes referred to as corrigenda.</p
></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-example</p></td>
<td style="vertical-align:top"><p>An illustration of a key concept
of the work, such as a code listing, case study or problem.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-footnote</p></td>
<td style="vertical-align:top"><p>Ancillary information, such as a
citation or commentary, that provides additional context to a referenced
passage of text.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-foreword</p></td>
<td style="vertical-align:top"><p>An introductory section that precedes
the work, typically not written by the author of the work.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-glossary</p></td>
<td style="vertical-align:top"><p>A brief dictionary of new, uncommon
or specialized terms used in the content.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-glossref</p></td>
<td style="vertical-align:top"><p>A reference to a glossary definition.</p
></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-index</p></td>
<td style="vertical-align:top"><p>A navigational aid that provides
a detailed list of links to key subjects, names and other important
topics covered in the work.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-introduction</p></td>
<td style="vertical-align:top"><p>A preliminary section that typically
introduces the scope or nature of the work.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-noteref</p></td>
<td style="vertical-align:top"><p>A reference to a footnote or endnote,
typically appearing as a superscripted number or symbol in the main
body of text.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-notice</p></td>
<td style="vertical-align:top"><p>Notifies the user of consequences
that might arise from an action or event. Examples include warnings,
cautions and dangers.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-pagebreak</p></td>
<td style="vertical-align:top"><p>A separator denoting the position
before which a break occurs between two contiguous pages in a statically
paginated version of the content.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-pagelist</p></td>
<td style="vertical-align:top"><p>A navigational aid that provides
a list of links to the pagebreaks in the content.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-part</p></td>
<td style="vertical-align:top"><p>A major structural division in a
work that contains a set of related sections dealing with a particular
subject, narrative arc or similar encapsulated theme.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-preface</p></td>
<td style="vertical-align:top"><p>An introductory section that precedes
the work, typically written by the author of the work.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-prologue</p></td>
<td style="vertical-align:top"><p>An introductory section that sets
the background to a work, typically part of the narrative.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-pullquote</p></td>
<td style="vertical-align:top"><p>A distinctively placed or highlighted
quotation from the current content designed to draw attention to a
topic or highlight a key point.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-qna</p></td>
<td style="vertical-align:top"><p>A section of content structured
as a series of questions and answers, such as an interview or list
of frequently asked questions.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-subtitle</p></td>
<td style="vertical-align:top"><p>An explanatory or alternate title
for the work, or a section or component within it.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-tip</p></td>
<td style="vertical-align:top"><p>Helpful information that clarifies
some aspect of the content or assists in its comprehension.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p>doc-toc</p></td>
<td style="vertical-align:top"><p>A navigational aid that provides
an ordered list of links to the major sectional headings in the content.
A table of contents may cover an entire work, or only a smaller section
of it.</p></td>
</tr>
</tbody>
</table>

Accessibility
-------------

Apply the following points to make the output accessible (recommended
practice).

-   Image should be provided with alt text (if provided by customer) and
    decorative images should be left blank

-   All the elements should be marked with appropriate tags. See links
    for more detail. \
    <http://kb.daisy.org/publishing/>\
    <https://idpf.github.io/a11y-guidelines/>

-   Color contrast should be 4.5:1 which can be checked through ACE epub
    accessibility checker

-   Zoom the text to 200% and ensure that the epub file remains readable
    without any text cut issues

-   Text should not be captured as image

-   Each HTML page should have proper title and the title should reflect
    the page title

-   Language of the page should be defined and any other language text
    inside the content should be defined with proper language code

