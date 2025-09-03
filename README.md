# Fulcrum EPUB Specification
The Fulcrum EPUB Specification is designed to help ebook production vendors and publishers create EPUB files compatible with the Fulcrum platform's Reading System. This specification does not repeat conformance requirements contained in the official EPUB specification. However, requirements and techniques regarding file and directory structure, naming conventions, treatments for images, time-based media, navigation, metadata, accessibility, HTML and other such details are included in this specification.

Wherever possible, the Fulcrum EPUB Specification follows the recommendations and techniques in the [DAISY Accessible Publishing Knowledge Base](http://kb.daisy.org/publishing/docs/) but offers scholarly monograph specific examples or techniques Fulcrum prefers.

If you have questions, feedback, or find errors or issues with this specification, [please file an issue within the project](https://github.com/mlibrary/fulcrum-epub-spec/issues/new) or email fulcrum-info@umich.edu. 

## Contents

- [1.0 Target Specification -- EPUB3](#10-target-specification----epub3)

- [1.1 EPUB Version](#11-epub-version)

- [1.2 Element Specification for Reformatting](#12-element-specification-for-reformatting)

	- [1.2.1 Standard Functionality Levels for PDF source](#121-standard-functionality-levels-for-pdf-source)

- [1.3 File Name](#13-file-name)

- [1.4 Folder Structure](#14-folder-structure)

	- [1.4.1 Optional File Inclusions](#141-optional-file-inclusions)

- [1.5 EPUB Package](#15-epub-package)

- [1.6 General Metadata](#16-general-metadata)

	- [1.6.1 Dublin Core](#161-dublin-core)

- [1.7 Accessibility Metadata](#17-accessibility-metadata)
  
	- [1.7.1 Schema.org Accessibility Metadata](#171-schemaorg-accessibility-metadata)
	  
	- [1.7.2 ONIX Accessibility Metadata](#172-onix-accessibility-metadata)

- [1.8 Navigation](#18-navigation)
  
	- [1.8.1 Table of Contents](#181-table-of-contents)
	  
	- [1.8.2 Landmarks](#182-landmarks)
	
	- [1.8.3 Page List](#183-page-list) 
  
- [1.9 HTML Meta Header](#19-html-meta-header)
  
- [1.10 Language](#110-language)

- [1.11 HTML Title](#111-html-title)

- [1.12 Headings](#112-headings)

	- [1.12.1 Numbered headings](#1121-numbered-headings)

	- [1.12.2 Separate heading and subtitle](#1122-separate-heading-and-subtitle)

	- [1.12.3 Merged heading and subtitle](#1123-merged-heading-and-subtitle)

- [1.13 Tables](#113-tables)

	- [1.13.1 Column heads and row heads](#1131-column-heads-and-row-heads)
	  
	- [1.13.2 Large tables](#1132-large-tables)
	  
	- [1.13.3 Irregular header](#1133-irregular-header)

	- [1.13.4 Complex headings](#1134-complex-headings)

	- [1.13.5 Layered headings](#1135-layered-headings)

- [1.14 Lists](#114-lists)

	- [1.14.1 Unordered list](#1141-unordered-list)

	- [1.14.2 Definition list](#1142-definition-list)

    - [1.14.3 Items requiring list encoding](#1143-items-requiring-list-encoding)
	  
- [1.15 Epigraphs, Dialogue, Poetry](#115-epigraphs-dialogue-poetry)

- [1.16 Links](#116-links)

	- [1.16.1 Guidelines for links](#1161-guidelines-for-links)

	- [1.16.2 Link with full context of destination](#1162-link-with-full-context-of-destination)

	- [1.16.3 Link with alternate text](#1163-link-with-alternate-text)
	  
	- [1.16.4 Link format for DOIs](#1164-link-format-for-dois)

	- [1.16.5 Visual distinctive linking](#1165-visual-distinctive-linking)

- [1.17 Images and Media](#117-images-and-media)

	- [1.17.1 Acceptable image and media file types](#1171-acceptable-image-and-media-file-types)
	  
	- [1.17.2 Recommended image criteria](#1172-recommended-image-criteria)
	  
	- [1.17.3 Significant simple image](#1173-significant-simple-image)

	- [1.17.4 Decorative image](#1174-decorative-image)
	  
	- [1.17.5 Cover image](#1175-cover-image)

	- [1.17.6 Figures](#1176-figures)

	- [1.17.7 Extended description via hyperlink](#1177-extended-description-via-hyperlink)

	- [1.17.8 Fulcrum Resource References](#1178-fulcrum-resource-references)
	  
	- [1.17.9 Figure, image, and media placement](#1179-figure-image-and-media-placement)

- [1.18 Code Blocks](#118-code-blocks)

	- [1.18.1 Inline Code](#1181-inline-code)

	- [1.18.2 Code Blocks](#1182-code-blocks)

	- [1.18.3 Code Blocks with Line Numbers](#1183-code-blocks-with-line-numbers)

	- [1.18.4 Code Blocks with Line Numbers as Tables](#1184-code-blocks-with-line-numbers-as-tables)

	- [1.18.5 Comparing Code Blocks with Line Numbers](#1185-comparing-code-blocks-with-line-numbers)

- [1.19 Footnotes and Endnotes](#119-footnotes-and-endnotes)

	- [1.19.1 Footnotes in the body](#1191-footnotes-in-the-body)

	- [1.19.2 Endnote section](#1192-endnote-section)

	- [1.19.3 Back-linking notes](#1193-back-linking-notes)

- [1.20 Bibliographies](#120-bibliographies)
  
- [1.21 Indexes](#121-indexes)
  
- [1.22 Content Numbering](#122-content-numbering)

	- [1.22.1 Page Break Numbering](#1221-page-break-numbering)

	- [1.22.2 Paragraph Numbering](#1222-paragraph-numbering)

	- [1.22.3 Line Numbering](#1223-line-numbering)
  
- [1.23 Chapters split into multiple XHTML files](#122-chapter-split)

- [1.24 CSS Stylesheet](#124-css-stylesheet)

	- [1.24.1 Standard CSS Stylesheets](#1241-standard-css-stylesheets)

	- [1.24.2 CSS Units](#1242-css-units)

	- [1.24.3 Colors](#1243-colors)

	- [1.24.4 Background Images](#1244-background-images)

	- [1.24.5 Hidden Content](#1245-hidden-content)

	- [1.24.6 CSS Property Reference](#1246-css-property-reference)

	- [1.24.7 CSS 2.1 Pseudo-Classes](#1247-css-21-pseudo-classes)

	- [1.24.8 CSS 2.1 Pseudo-Elements](#1248-css-21-pseudo-elements)

- [1.25 Fonts](#125-fonts)

- [1.26 Formatting](#126-formatting)

- [1.27 Boxed Text](#127-boxed-text)

- [1.28 Marginalia and Sidebars](#128-marginalia-and-sidebars)

- [1.29 Reading Order](#129-reading-order)

- [1.30 DPUB ARIA Semantics](#130-dpub-aria-semantics)

- [1.31 Accessibility](#131-accessibility)

- [Revision History](#revision-history)

# 1.0 Target Specification -- EPUB3

## 1.1 EPUB Version
[EPUB version 3.3](https://www.w3.org/publishing/epub3/) is the recommended technical specification for EPUB created for submission to Fulcrum. EPUB 3.0+ will function correctly in the Fulcrum Reader.

EPUB conforming to a specification less than EPUB 3.0 will not function as expected in the Fulcrum Reader and should be converted to EPUB 3.0+ before submission to Fulcrum whenever possible.

- EPUB 3.3 must be validated against [EPUBCheck version 5.2.1](https://github.com/w3c/epubcheck/releases/tag/v5.2.1).
- XHTML files should be compliant with HTML5.

### Required For
| U-M Vendor        | Fulcrum Partner   |
| ----------------- | ----------------- |
| Must be EPUB 3.0+ | Must be EPUB 3.0+ |

## 1.2 Element Specification for Reformatting
The following matrix details recommendations for converting different elements from PDF to EPUB 3.

### 1.2.1 Standard Functionality Levels for PDF source
When converting backlist titles from PDF to EPUB3, use the following table a guide for conversion.

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

**<span class="underline">Note</span>:** If the input is EPUB, then output should be in the same format.

### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No |

## 1.3 File Name
The EPUB3 output file name will be the 13-digit ISBN number of the same input file name.

The use of the 13-digit ISBN number of the source file is optional for third-party partners to Fulcrum. However, file naming conventions must be consistent across titles submitted to Fulcrum.

### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No |

## 1.4 Folder Structure
The following folder structure is required for vendor deliverables to Michigan Publishing. The folder structure below is optional for third-party partners to Fulcrum. However, folder structure conventions must be consistent across titles submitted to Fulcrum.

The EPUB should conform to the following directory structure and naming convention.

<pre>
<b>/META-INF</b>
    <b>container.xml</b>
<b>/OEBPS</b>
    <b>/xhtml/<i>FileName-xxy</i>.xhtml</b>
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

Where:

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

### Required For
| U-M Vendor | Fulcrum Partner |
| ---------- | --------------- |
| Yes        | No              |

### 1.4.1 Optional File Inclusions

Additional inclusions supporting EPUB reading systems, such as iBooks and the com.apple.ibooks.display-options.xml file, is permissible and will not interfere with the Fulcrum Reader.

If such files are in the source file provided for conversion, they will be in the deliverable EPUB3.

## 1.5 EPUB Package
The EPUB3 output contains the following folders and files.

-   XHTML files
-   Image files
-   toc.ncx
-   toc.xhtml (contains `epub:type="landmarks"` and  `epub:type="page-list"`)
-   mimetype
-   container.xml
-   content.opf
-   Stylesheets (CSS)
-   Embedded Fonts (only if approved)

### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No |

## 1.6 General Metadata

If the EPUB is a derivative of a print source, include the `pageBreakSource` metadata:

```
<meta property="pageBreakSource">urn:isbn:9780472132034</meta>
```

**NOTE**: if the EPUB must pass EPUBCheck less than 5.0, use the encoding practice specified below in 1.6.1 Dublin Core: Source instead.

### Required For
| U-M Vendor | Fulcrum Partner |
| ---------- | --------------- |
| Yes        | Yes             |

### 1.6.1 Dublin Core
Dublin Core metadata is required for the following items:

-   Title
-   Creator
-   Language
-   Rights
-   Publisher
-   Identifier
-   Source
	- Note: Only required when the EPUB is a derivative of a print source AND the EPUB must be validated against a version of EPUBCheck less than version 5. See additional fields also needed in example below.
- Date

**Example code:**

````
<dc:title>A Mid-Republican House from Gabii</dc:title>
<dc:creator>Rachel Opitz</dc:creator>
<dc:creator>Marcello Mogetta</dc:creator>
<dc:creator>Nicola Terrenato</dc:creator>
<dc:language>en-US</dc:language>
<dc:rights>© University of Michigan Press</dc:rights>
<dc:publisher>University of Michigan Press</dc:publisher>
<dc:identifier id="BookID">9780472999002</dc:identifier>
<dc:source id="src-id">urn:isbn:9780472999999</dc:source>
<meta refines="#src-id" property="dcterms:issued">2000-01-01</meta>
<dc:date>2018-03-03</dc:date>
````

**NOTE**: The `dc:source` element and related `meta refines="#src-id"` are only to be included if the publisher requires EPUB to pass EPUBCheck version < 5.0.
### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | Yes |

## 1.7 Accessibility Metadata
Include the two types of accessibility metadata -- schema.org and ONIX -- defined in the current EPUB environment.

### 1.7.1 Schema.org Accessibility Metadata
> Schema: <http://kb.daisy.org/publishing/docs/metadata/schema-org.html>

EPUB must contain the following schema properties:

- `accessibilityFeature`
- `accessibilityHazard`
- `accessibilitySummary`
- `accessMode`
- `accessModeSufficient`

EPUB that include accessibility conformance and certification information must also contain:

```
<meta property="dcterms:conformsTo" id="conf"> EPUB Accessibility 1.1 - WCAG 2.2 Level AA </meta>

<meta property="a11y:certifiedBy" refines="#conf" id="certifier">[Certifier Name]</meta>

<meta property="a11y:certifierCredential" refines="#certifier">[URL to Certifier Credential]</meta>
```

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No, but strongly recommended |

### 1.7.2 ONIX Accessibility Metadata

> ONIX: <http://kb.daisy.org/publishing/docs/metadata/onix.html>

Use ONIX only when creating a separate ONIX metadata XML to place in the /meta folder of the EPUB.

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| No | No |

## 1.8 Navigation
### 1.8.1 Table of Contents
In the `nav epub:type="contents"`, typically in the `toc.xhtml` file, include the following EPUB sections as follows (if section is applicable):

-  Cover
-  Title
    -   Note: If there are multiple title pages, label the contents "Title Page" and "Original Title Page".
-  Half Title
-  Copyright
    -   Note: If there are multiple copyright pages (e.g., the Routledge Revivals imprint which contains the original copyright page usually from the 1800s), the contents are to be labeled "Copyright Page" and "Original Copyright Page".
-  Dedication
-  Table of Contents page
    -  Note: If the Table of Contents is missing for a title, raise a JIRA ticket to see if the client can resupply the file. If not, construct a Table of Contents page fom the Chapter Titles.
-  All Lists of Tables, Figures, Illustrations, Maps, etc.  
-  All book sections listed in the Table of Contents
-  Appendices
-  Bibliographies
-  Endnotes
-  Indexes

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No, but strongly recommended |

### 1.8.2 Landmarks
In the  `<nav epub:type="landmarks">`, typically in the `toc.xhtml` file, include the following EPUB sections as follows (if section is applicable):

- Cover
- Table of Contents page
-  All lists of Tables, Figures, Illustrations, Maps, Appendices etc.
-  Start of content (typically the first major section after the front matter)  
-  Appendices
-  Bibliographies
-  Endnotes
-  Contributors
-  Indexes

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No, but strongly recommended |

### 1.8.3 Page List
If a print equivalent exists and page breaks are indicated within EPUB, include a page list in the `nav epub:type="page-list"`, typically in the `toc.xhtml` file, that includes a listing of all pages and links to those pages. See the [DAISY Accessible Publishing Knowledge Base for examples](https://kb.daisy.org/publishing/docs/navigation/pagelist.html).

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No, but strongly recommended |

## 1.9 HTML Meta Header
The following `<meta>` elements should placed inside the `<head>` element in all the XHTML files. The `viewport` tag scales the page to the device size (`initial-scale=1.0`) but allows the user to zoom the page up to 5x its initial size (`maximum-scale=5.0`). They are optional for Fulcrum partners.

**Example Code:**

````
<meta name="viewport" content="initial-scale=1.0,maximum-scale=5.0"/>
````

### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No, but strongly recommended |


## 1.10 Language
The primary language of the publication and shifts in primary language in body text should be set to ensure that assistive technologies correctly interpret and render the text.

The primary language should be placed in `lang` and `xml:lang`  attributes inside the `<html>` element in all the XHTML files. 

**Example Code:**

````
<html ... lang="en" xml:lang="en">
````

Shifts in primary language in the body text, footnotes, or references should override the set language by wrapping the content in `<span>` element with  `lang` and `xml:lang` attributes.

**Example Code:**

```
<html ... lang="en" xml:lang="en">
	...
	<body>
		...
		<section>
		<p>Newspapers in the People’s Republic were to 
		function as communication channels for transmitting 
		the central Party leaders’ positions and policies 
		out to the nation’s provinces and counties, and 
		relaying the conditions and experiences of the local 
		masses and ground level (<span lang="zh-Hans" 
		xml:lang="zh-Hans"><i>jiceng</i></span>) cadres back 
		up to the central Party (A. P. L. Liu 1971; Schurmann 
		1966).</p>
		...
		</section>
		...
	</body>
</html>
```

Language attribute values must be valid. The [W3C provides guidance on selecting valid language tags](https://www.w3.org/International/questions/qa-choosing-language-tags).

### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No |

## 1.11 HTML Title
Assigning meaningful titles is a recommended best practice for \<title\> elements in the EPUB. Such titles help all users to find and navigate through the documents, and, are essential for screen reader users.

**Example 1. One chapter/part per HTML**

````
<html ...>
<title>Chapter 1. Democratic Communications Infrastructure, Discourse, Policy, and Advocacy</title>
````

**Example 2. Multiple HTML files for one chapter/part**

If a chapter or part is split into multiple HTML files, the following method should be followed.

````
<html ...>
<title>Chapter 1. Continued (2 of 3). Democratic Communications Infrastructure, Discourse, Policy, and Advocacy</title>
````

### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | Yes |

## 1.12 Headings

Apply heading tags as per the HTML element for the headings. Ensure all headings are identified. Based on the heading levels, apply heading tags ranging from h1 to h6 as needed. Do not skip heading levels.

### 1.12.1 Numbered headings
Heading numbers should decrease by one for each subsection. Never skip a heading number.

````
<section role="doc-chapter">
	<h1>Chapter 1 Democratic Communications Infrastructure, Discourse, Policy, and Advocacy</h1>
	...
	<section>
		<h2>The Discourse of “Net Neutrality”</h2>
		...
		<section>
		<h3>On "Net Neutrality"</h3>
		...
		</section>
		...
	</section>
	...
</section>
````

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | Yes |

### 1.12.2 Separate heading and subtitle

The title and subtitle are contained in separate elements, but grouped in a header element to better associate them. Use the role `doc-subtitle` to identify the subtitle.

````
<section id="pref" aria-labelledby="headerpref01">      
	<header id="headerpref01">
		<h1 class="ctfm">Preface</h1>
		<p role="doc-subtitle" class="cs">Navigating Deep Waters</p>
	</header>
	...
</section>
````

**NOTE**: current best practice recommends wrapping the heading element in `hgroup` instead of `header`, but due to limitations in U-M's ebook distribution and EPUBCheck validation, `header` should be used instead until further notice.
#### Required For
| U-M Vendor | Fulcrum Partner |
| ---------- | --------------- |
| Yes        | No              |

### 1.12.3 Merged heading and subtitle

When the subtitle is contained within the same heading element as the title, identify it in a span with the role of doc-subtitle.

````
<section role="doc-chapter">
	<h1>Chapter 1  
        <span role="doc-subtitle">Democratic Communications Infrastructure, Discourse, Policy, and Advocacy</span>
	</h1>
````

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| No | No |

## 1.13 Tables
Ensure all tabular data is marked up using `table` tags, that titles are provided in a `<caption>` element, and that header cells are identified in the `scope` attribute. Headers should be contained within a `thead` element and footers within a `tfoot` element. The rows that represent the body of the table should be contained within a `tbody` element.

### 1.13.1 Column heads and row heads
Column heads and row heads must be defined as headers with appropriate scope attributes. The `scope` attribute should contain a `col`, `colgroup`, `row`, or `rowgroup` value wherever required.

```
<table>
	<thead>
	<tr>
		<td></td>
		<th scope="col" class="tch">Emigration tax revenue<a id="tn2r" class="tnref" href="Kreutzmuller_Dispossession-0012.xhtml#tn2">a</a></th>
		<th scope="col" class="tch">Implied capital</th>
		<th scope="col" class="tch">Estimated transfer quota</th>
		<th scope="col" class="tch">Taxed / Immobilized</th>
		<th scope="col" class="tch">Implicit emigration tax rate</th>
		<th scope="col" class="tch">For comparison: Bajohr (2003)</th>
	</tr>
	</thead>
	<tbody>
	<tr>
		<th scope="row"><p class="td">1933</p></th>
		<td><p class="td">17.602</p></td>
		<td><p class="td">70.408</p></td>
		<td><p class="td">50%</p></td>
		<td><p class="td">44.005</p></td>
		<td><p class="td">62.5%</p></td>
		<td><p class="td">20%</p></td>
	</tr>
	...
	</tbody>
</table>
```


### 1.13.2 Large tables
If a table exceeds more than 8 columns or its layout could be compromised in its presentation on a Reading System, it is acceptable to present the table as an image. However, in such cases you must also provide a link to an XHTML file outside of the linear flow of the EPUB that contains the HTML version of the large table. Users with text-to-speech playback available will be able to navigate the markup regardless of the rendering quality. 

See the technique in section 1.15.4 for providing an extended description of an image as guidance for including images of tables.

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No |

### 1.13.3 Irregular header

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

````
<table border="1">
<colgroup span="2"/>
<colgroup span="1"/>
<colgroup span="2"/>
<colgroup span="2"/>
<colgroup span="1"/>
<thead>
<tr>
<th id="ship" colspan="2" scope="colgroup">Shipping.</th>
<th id="stock" rowspan="2" scope="colgroup">Stock.</th>
<th id="wages" colspan="2" scope="colgroup">Wages.</th>
<th id="wt" colspan="2" scope="colgroup">Weights.</th>
<th id="name" rowspan="2" scope="colgroup">Name of Colony.</th>
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
...
</tbody>
</table>
````

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No |

### 1.13.4 Complex headings

The following table shows a distance chart with the start destinations defined in the first row and at the end destination at the end of each subsequent row. 

In this case, because the header is at the end of the row setting a scope of "`row`" does not apply it back to the cells already encountered. The `headers` attribute must be applied to each cell.

<table>
   <tr>
      <th id="van">Vancouver</th>
      <th id="cal">Calgary</th>
      <th id="sask">Saskatoon</th>
      <th id="win">Winnipeg</th>
      <th id="tor">Toronto</th>
      <th id="mon">Montreal</th>
      <th id="stj">St. John's</th>
      <th></th>
   </tr>
   <tr>
      <td headers="van stj-dest">7323</td>
      <td headers="cal stj-dest">6334</td>
      <td headers="sask stj-dest">5838</td>
      <td headers="win stj-dest">5010</td>
      <td headers="tor stj-dest">3141</td>
      <td headers="mon stj-dest">2602</td>
      <td headers="stj stj-dest">0</td>
      <th id="stj-dest">St. John's</th>
   </tr>
   
   <tr>
      <td headers="van mon-dest">4271</td>
      <td headers="cal mon-dest">3743</td>
      <td headers="sask mon-dest">3232</td>
      <td headers="win mon-dest">2408</td>
      <td headers="tor mon-dest">539</td>
      <td headers="mon mon-dest">0</td>
      <td headers="stj mon-dest">2602</td>
      <th id="mon-dest">Montreal</th>
   </tr>
   …
</table>

Use `scope="col"` to make the start destinations the column headers and
`scope="row"` to make the end destinations the row headers:

````
<table>
   <tr>
      <th id="van">Vancouver</th>
      <th id="cal">Calgary</th>
      <th id="sask">Saskatoon</th>
      <th id="win">Winnipeg</th>
      <th id="tor">Toronto</th>
      <th id="mon">Montreal</th>
      <th id="stj">St. John's</th>
      <th></th>
   </tr>
   <tr>
      <td headers="van stj-dest">7323</td>
      <td headers="cal stj-dest">6334</td>
      <td headers="sask stj-dest">5838</td>
      <td headers="win stj-dest">5010</td>
      <td headers="tor stj-dest">3141</td>
      <td headers="mon stj-dest">2602</td>
      <td headers="stj stj-dest">0</td>
      <th id="stj-dest">St. John's</th>
   </tr>
   
   <tr>
      <td headers="van mon-dest">4271</td>
      <td headers="cal mon-dest">3743</td>
      <td headers="sask mon-dest">3232</td>
      <td headers="win mon-dest">2408</td>
      <td headers="tor mon-dest">539</td>
      <td headers="mon mon-dest">0</td>
      <td headers="stj mon-dest">2602</td>
      <th id="mon-dest">Montreal</th>
   </tr>
   …
</table>

````

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No |

### 1.13.5 Layered headings

The following table combines headers from the top of each column and beginning of each row:

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

The `headers` attribute is used to provide the IDs of the cells that contain the relevant heading text:

````
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
````

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No |

## 1.14 Lists

Tag list items with proper list tags to ensure semantic encoding. Do not use other elements such as `<p>` or bullet characters to denote a list item. By tagging the list items with proper list elements, the screen reader users can perceive meaningful information and will know that they are reading list items.

### 1.14.1 Unordered list

````
<ul>
	<li>Credit, consumer, 164</li>
	<li>Cross-functional contact, 10-11</li>
	<li>Culture
	<ul>
		<li>buyer behavior and, 85</li>
		<li>defined, 85, 98, 118</li>
...
	</ul>
	</li>
...
</ul>
````

Excerpt from: *Core Concepts of Marketing* --- John Burnett

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No |

### 1.14.2 Definition list

````
<dl>
  <dt><dfn>Exchange function</dfn></dt>
  <dd>
   Sales of the product to the various members
   of the channel of distribution.
  </dd>
  <dt><dfn>Physical distribution function</dfn></dt>
  <dd>
   Moves the product through the exchange
   channel, along with title and ownership.
  </dd>
  <dt><dfn>Marketing channel</dfn></dt>
  <dd>
   Sets of independent organizations involved
   in the process of making a product or
   service available for use or consumption
   as well as providing a payment mechanism
   for the provider.
  </dd>
 ...
</dl>
````

Excerpt from: *Core Concepts of Marketing* --- John Burnett

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No |

### 1.14.3 Items requiring list encoding
In addition to lists appearing in body content, other recurring content that must be encoded as a list includes:

* Lists of titles on Series pages (unordered list).
* Table of Contents pages (ordered list).
* Lists of figures/illustrations (ordered list).
* Lists of tables (ordered list).
* Endnotes (ordered list). See [1.19.2 for details](#1192-endnote-section).
* Bibliographies (ordered list). See [1.20 for details](#120-bibliographies).
* Indexes (unorded list). See [1.21 for details](#121-indexes).

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No |

## 1.15 Epigraphs, Dialogue, Poetry

When these elements are styled as quotes, they should be implemented with the use of the `blockquote` element.

```
<blockquote class="senseline">  
    <p class="slf">In the dry season, someone must be the first drop of rain.</p>  
    <p class="sll">Let it be me. Let it begin with me.</p>  
</blockquote>
```

Special attention should be paid to epigraphs that have attribution or bylines. These need `blockquote` and to be wrapped in `figure` element.

```
<figure>  
	<blockquote role="doc-epigraph" class="epigraph">  
       <p class="eps"><span lang="kyh" xml:lang="kyh">“kúna vúra kúkuum ôok tá ni’uum, pananífyiivshas nimúsarukti, kári vúra pakáruk váhi ni’aapúnmiikti.”</span></p>  
    </blockquote>  
    <figcaption>  
       <p class="ept">—William Bright, Speech to Karuk Tribal Council, 2004</p>  
    </figcaption>  
</figure>
```
## 1.16 Links

The recommended best practice is to include links as meaningful text if the surrounding text is inadequate to define the purpose of the link. By providing meaningful text interpretation, the screen reader user can understand the purpose of the link and decide if they need to navigate
to that particular link. 

Overuse of links, while may seemingly helpful, can create complex navigational experiences for assistive technology readers. Always ensure that links are useful and not adding additional complexity when deciding to include. As such, it is best to avoid back linking chapter titles to the TOC page whenever possible.

### 1.16.1 Guidelines for links

All the cross-references such as notes and footnotes are two-way linked. Other references such as page, section, figure, etc., are one-way linked. The web address and email address links are active.

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No |

### 1.16.2 Link with full context of destination

The user can determine the destination of the link from the text of the \<a\> element alone.

````
<p>For more information, refer to <a href="#...">Section 1.1 of Web Publications</a></p>
````

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| No | No |


### 1.16.3 Link with alternate text

Adding alternate text is an optional best practice if neither of the above conditions are met. Use the title attribute to provide additional context.

````
<a href="#..." title="The EPUB specifications">click here</a>
````

#### Required For
| U-M Vendor | Fulcrum Partner |
| ---------- | --------------- |
| No         | No              |

### 1.16.4 Link format for DOIs
When using DOIs in any section of the EPUB, the title of the publication should be included in an `aria-label` attribute. See the [CrossRef Accessibility Guidelines](https://www.crossref.org/blog/accessibility-for-crossref-doi-links-call-for-comments-on-proposed-new-guidelines/) for more details.

````
<a href="https://doi.org/10.5555/12345678" aria-label="DOI for Toward a Unified Theory of High-Energy Metaphysics: Silly String Theory">https://doi.org/10.5555/12345678</a>
````

#### Required For

| U-M Vendor | Fulcrum Partner |
| ---------- | --------------- |
| Yes        | No              |

### 1.16.5 Visual distinctive linking

**Bold Text Option:** By specifying bolder, either a medium font or a bold one will make links visually stand out from their surrounding text.

````
a {
    text-decoration: none;
    font-weight: bolder;
    color: rgb(51,102,204);
  }
````

**Dotted Border Option:** A dotted border is placed under all links to highlight them instead of a line.

````
a {
    text-decoration: none;
    padding-bottom: 0.3rem;
    border-bottom: 0.1rem dotted rgb(100,100,100);
  }
````

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| No | No |

## 1.17 Images and Media

The name assigned to an image file contained within the EPUB should not contain spaces.
The underscore or dash characters should be used in place of spaces.
#### Required For
| U-M Vendor | Fulcrum Partner |
| ---------- | --------------- |
| Yes        | Yes             |

### 1.17.1 Acceptable Image and Media File Types

Acceptable file types for images include JPG, PNG and SVG.

Acceptable file types for video include MPEG-4 (.mp4, .m4v), Quicktime (.mov), and AVI (.avi) formats.

Acceptable file types for audio include WAV and MPEG 3 (.mp3).

### 1.17.2 Recommended Image Criteria

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
<td style="vertical-align:top"><p>Reference <a href="https://github.com/mlibrary/fulcrum-epub-spec/blob/master/fulcrum.css">Fulcrum Generic EPUB CSS</a></p></td>
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

**Note**: For EPUB source files, retain the images as per the source EPUB file with the aforementioned properties.
#### Required For
| U-M Vendor | Fulcrum Partner              |
| ---------- | ---------------------------- |
| Yes        | No, but strongly recommended |


### 1.17.3 Significant simple image
Images should have an alternate text (`img/@alt` attribute) for screen reader users. By providing an alternate text for non-visual content, the screen reader users can perceive information about the image through the alternate text provided by us.

````
<img src="covers/9781449328030_lrg.jpg" alt="Accessible EPUB 3 - First Edition"/>
````

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No, but strongly recommended |

### 1.17.4 Decorative image

An empty `alt` attribute is complimented by the `role` presentation to indicate that the image contains no information for users.

````
<img src="graphics/gothic-border.png" role="presentation" alt=""/>
````

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No, but strongly recommended |

### 1.17.5 Cover Image

<table>
<tbody>
<tr>
<td style="vertical-align:top"><p><b>1.17.5.1</b></p></td>
<td style="vertical-align:top"><p>The cover must consist of an XHTML file containing nothing but an image. The image must be styled to take up the entire height of the screen. This can be achieved using the CSS below (just an example) or follow sample CSS if available:</p
><pre>img.cover {
    height: 100%;
}</pre></td>
</tr>
<tr>
<td style="vertical-align:top"><p><b>1.17.5.2</b></p></td>
<td style="vertical-align:top"><p>Declare the cover in metadata (OPF) (mandatory).</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p><b>1.17.5.3</b></p></td>
<td style="vertical-align:top"><p>Capture cover related metadata as follows in .opf file:</p><pre>&lt;meta name="cover" content="cover-image" />&lt;item id="cover-image" href="images/cover.jpg" media-type="image/jpeg"/></pre></td>
</tr>
<tr>
<td style="vertical-align:top"><p><b>1.17.5.4</b></p></td>
<td style="vertical-align:top"><p>Minimum width of the cover should be more than 600 px and minimum height of the cover should be 800 px captured proportionately.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p><b>1.17.5.5</b></p></td>
<td style="vertical-align:top"><p>If the cover size of the source EPUB file is too small, then retain the cover per the source EPUB cover. Do not increase the size of the source EPUB cover.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p><b>1.17.5.6</b></p></td>
<td style="vertical-align:top"><p>The cover image needs to fit the page when viewed in the Fulcrum Reading System to cover as much white space as possible.</p></td>
</tr>
<tr>
<td style="vertical-align:top"><p><b>1.17.5.7</b></p></td>
<td style="vertical-align:top"><p>Never exclude the cover XHTML page from the linear flow of the EPUB. In the .opf file, it should be encoded as part of the flow:</p> <pre>&lt;spine toc="ncx"> 
 &lt;itemref idref="cover" linear="yes"/>
  ...
&lt;/spine></pre> 

<p>If the cover XHTML file is defined outside of the linear flow, the EPUB will not work in the Fulcrum Reading System.</p></td>
</tr>
</tbody>
</table>

#### Required For
| U-M Vendor | Fulcrum Partner              |
| ---------- | ---------------------------- |
| Yes        | No, but strongly recommended |

### 1.17.6 Figures

For a group that consists of an image and an associated caption, the `figure` and `figcaption` elements should be used. One or more `img` elements may exist within the `figure` element, but only one `figcaption` element should exist. The `figcaption` element should exist after its associated `img` element(s).

Below is an example of two images with a single caption:

````
<figure role="group">
    <img src="chart1.png" 
         alt="Bar chart showing monthly and total visitors for 
            the first quarter 2014 for sites 1 to 3"/>
    <img src="chart2.png" 
        alt="Bar chart showing monthly and total visitors for 
            the first quarter 2014 for sites 4 to 6"/>
    <figcaption>
    Example.com Site visitors Jan to March 2014 text description of the bar chart
    </figcaption>
</figure>
````

**NOTE:** the `img` element should be a direct child of the `figure` element and not wrapped within another container such as a `p` or a `div`.

If multiple images and captions are to be grouped together, then nested `figure` elements are to be used. 

**Code example:**

````
<figure role="group" aria-labelledby="fig1">
    <figure role="group" aria-labelledby="fig11">
        <img src="castle-etching.jpg"
	        alt="The castle has one tower, and a tall wall around it.">
        <figcaption id="fig11">
        Charcoal on  wood. Anonymous, circa 1423.
        </figcaption>
    </figure>
    <figure role="group" aria-labelledby="fig12">
        <img src="castle-painting.jpg"
	        alt="The castle now has two towers and two walls.">
        <figcaption id="fig12">
        Oil-based paint on canvas. Eloisa Faulkner, 1756.
        </figcaption>
    </figure>
    <figure role="group" aria-labelledby="fig13">
        <img src="castle-fluro.jpg"
	        alt="The castle lies in ruins, the original tower all that remains in one piece.">
        <figcaption id="fig13">
        Film photograph. <span lang="fr">Séraphin Médéric Mieusement</span>, 1936.
        </figcaption>
    </figure>
    <figcaption id="fig1">
    The castle through the ages: 1423, 1756, and 1966 respectively.
    </figcaption>
</figure>
````

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No |

### 1.17.7 Extended description via hyperlink

Extended description inclusion and linking via a hyperlink should be provided for complex images such as charts, graphs, maps, and images with text. Linking via a hyperlink is optional unless the description is provided in the source.

The following example uses a simple text hyperlink below the image to link to a separate XHTML file containing only one extended description, and provides a text hyperlink to return back to original reading position. **The separate XHTML file with extended description should be placed at the end of the spine and outside the linear flow of the EPUB contents.**

See the [DAISY Consortium's Best Practices for Authoring Extended Descriptions](https://daisy.github.io/transitiontoepub/best-practices/extended-desc/ExtendedDescriptionsBestPractices.html) for other techniques and additional details.

Below is an example of Fulcrum's preferred technique of extended description with hyperlink pointing to the full description. The following example uses figure and figcaption elements, but the technique can also be used without these elements.

```
<figure id="f131" class="figure">
      	<p class="fig"><img src="images/Fig13_01.png" alt="Three pie charts illustrating the breakdowns of races, nationalities, and genders of composers of color in the most common music theory textbooks." aria-details="rFigure13.1" /></p>
      	<figcaption>
        	<p class="figh"><span class="fighn">Figure 13.1:</span> Composers of Color in the most common music theory textbooks</p>
      	</figcaption>	
</figure>
<p class="image-right_back"><a id="rFigure13.1" href="ExtDesc_Figure13_1.xhtml#Figure13.1">Follow for extended description of Figure 13.1</a></p>
```

If a `figure` contains 2 or more images with extended descriptions, the `figure` should either be A) broken into multiple `figure` elements, or, in the case where they share the caption, B) use nested figures with the description link after the child `figure`.

```
<figure role="group" aria-labelledby="fig1">
    <figure role="group" aria-labelledby="fig11">
        <img src="castle-etching.jpg"
	        alt="The castle has one tower, and a tall wall around it."/>
        <figcaption id="fig11">
        Charcoal on  wood. Anonymous, circa 1423.
        </figcaption>
    </figure>
    <p class="image-right_back"><a id="rlongdescription_01" href="Extended_desc01.xhtml#ilongdescription_01">Follow for extended description for Fig. 1</a></p>    
    <figure role="group" aria-labelledby="fig12">
        <img src="castle-painting.jpg"
	        alt="The castle now has two towers and two walls."/>
        <figcaption id="fig12">
        Oil-based paint on canvas. Eloisa Faulkner, 1756.
        </figcaption>
    </figure>
    <p class="image-right_back"><a id="rlongdescription_02" href="Extended_desc02.xhtml#ilongdescription_02">Follow for extended description for Fig. 2</a></p>
    <figure role="group" aria-labelledby="fig13">
        <img src="castle-fluro.jpg"
	        alt="The castle lies in ruins, the original tower all that remains in one piece."/>
        <figcaption id="fig13">
        Film photograph. <span lang="fr">Séraphin Médéric Mieusement</span>, 1936.
        </figcaption>
    </figure>
     <p class="image-right_back"><a id="rlongdescription_03" href="Extended_desc03.xhtml#ilongdescription_03">Follow for extended description for Fig. 3</a></p>   
     <figcaption id="fig1">
    The castle through the ages: 1423, 1756, and 1936 respectively.
    </figcaption>
</figure>
```

The extended description is contained within a separate XHTML file placed outside of the linear flow of the EPUB. It also shows a smaller image for convenience of the users. The separate file should be named `ExtDesc_Figure##_#.xhtml`. 

```
<?xml version="1.0" encoding="utf-8"?>
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml" xmlns:epub="http://www.idpf.org/2007/ops" lang="en-US" xml:lang="en-US">
	<head>
    	<meta name="viewport" content="initial-scale=1.0,maximum-scale=5.0" />
    	<title>Extended Description for Figure 13.1</title>
    	<link rel="stylesheet" type="text/css" href="default.css" />
    	<meta charset="UTF-8" />
	</head>
	<body>
    	<section aria-labelledby="Figure13.1">
        	<h1 class="chtitlel" id="Figure13.1">Extended Description for Figure 13.1</h1>
        	<div>
            	<p class="imgl"><img src="images/Fig13_01.png" alt="" role="presentation" /></p>
            	<p>The three pie charts present the following data. Race of Composers of Color (Black, 90%) and (Asian, 10%). Genders of Composers of Color (men, 85%) and (women 15%). Nationalities of Composers of Color (American, 85%), (Canadian, 2%), (Brazilian, 5%), (Chinese, 2% ), (French, 2%), (English, , 2%), and (Japanese, 2%). Values are estimated.
		</p>

            	<p class="image-right_back"><a role="doc-backlink" href="LucasPruett-0029.xhtml#rFigure13.1">Navigate back to Figure 13.1</a></p>
        	</div>
    	</section>
	</body>
</html>
```
In the `content.opf` file, place the XHTML description file at the end of the spine and keep the extended description out of the linear flow of the EPUB contents as in the example below:

```
<spine toc="ncx">
	<itemref idref="LucasPruett-0001"/>
	<itemref idref="LucasPruett-0002"/>
	<itemref idref="LucasPruett-0003"/>
	<itemref idref="LucasPruett-0004"/>
	<itemref idref="LucasPruett-0005"/>
	<itemref idref="LucasPruett-0006"/>
	<itemref idref="LucasPruett-0007"/>

       ...

	<itemref idref="ExtDesc_Figure13_1" linear="no"/>
  </spine>
```

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No |

### 1.17.8 Fulcrum Resource References

Once an EPUB is ingested in the Fulcrum platform, images, audio, or video referenced within EPUB content may be used to reference resources ingested in the platform. The `img` element may be replaced with markup that displays a resource such as a higher resolution image, audio, or video. The basename of the path (minus the extension) specified in the `img/@src` attribute value should match the basename of the resource. 

**Code example:**
````
<figure role="group">
    <img src="images/movie_trailer.jpg" 
         alt="Static image representing the movie trailer"/>
    <figcaption>
    Trailer for the movie.
    </figcaption>
</figure>
````
The path `images/movie_trailer.jpg`could match a video resource ingested in the Fulcrum platform that has the file name `movie_trailer.mp4`.

For the case where the `img/@src` value matches an ingested resource, but this instance should not be replaced, then the `img/@data-fulcrum-embed` attribute can be added to the `img` element:

````
<figure role="group">
    <img src="images/movie_trailer.jpg" 
         data-fulcrum-embed="false"
         alt="Static image representing the movie trailer"/>
    <figcaption>
    Trailer for the movie.
    </figcaption>
</figure>
````

To reference a Fulcrum resource within EPUB content at a location where no `img` element exists, the following markup may be used:

````
<figure style="display:none" data-fulcrum-embed-filename="Audio01.mp3">
    <figcaption>Additional Audio Resource</figcaption>
</figure>
````
The value of the `figure/@data-fulcrum-embed-filename` attribute contains the Fulcrum resource file name. Both the basename and the extension should match.

The `figcaption` element is optional, but can be used to provide a caption for the resource once it is displayed.

To reference a video on YouTube within EPUB content at a location where no `img` element exists, the following markup should be used:

````
<figure class="enhanced-media-display" data-fulcrum-embed-filename="[youtube video ID]"/>
````

With the placeholder value in the `data-fulcrum-embed-filename` attribute replaced with the YouTube Video ID.
#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| No | No |

### 1.17.9 Figure, Image, and Media Placement

For any object rendered as an image/graphic or media that occurs in the midst of a paragraph and interrupts text, it shall be placed either at the end of the preceding paragraph or the beginning of the nearest following paragraph within the specific page. Final placement of the image is dependent on the closest paragraph's proximity. The image must stay within the page marker it occurs on in the source PDF. If an image interrupts text, and no paragraph tag that starts or ends on the same page, then keep the image in its original location.

#### Required For
| U-M Vendor | Fulcrum Partner              |
| ---------- | ---------------------------- |
| Yes        | No, but strongly recommended |


## 1.18 Code Blocks

Representations of computer code within the text, referred to here as code blocks, should be encoded semantically when possible. Never use an image to represent lines of code, inline code, or code blocks.

### 1.18.1 Inline Code

Code to be displayed inline with paragraph text should be indicated with its equivalent semantic element.

````
<p>In table 2.2, the FizzBuzz algorithm ... is described as a
<i>loop</i> because it continues to compute results so long as the
proper conditions are met, in this case while the input amount
(<code>i</code>) is a number lower than or equal to 100.
Example 2.2.a, on the left, frames its computation in an initial
"catch-all" condition statement, that is, that <code>i</code>
is a multiple of three <i>or</i> of five. (The syntax
<code>i%3</code> checks whether "<code>i</code> divided by 3"
has a remainder of zero.) Then it checks each of those subconditions
independently of one another. This means that <code>i</code> ...
</p>
````

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No |

### 1.18.2 Code Blocks

Code that needs its formatting preserved and should display as a block of text, like a blockquote, should be identified a figure and be wrapped with elements to preserve formatting of the code. Note the application of the CSS class code on the figure element. Rules defined in the associate spec CSS file (see [fulcrum.css](https://github.com/mlibrary/fulcrum-epub-spec/blob/master/fulcrum.css)) help ensure formatting is preserved and line breaks occur when lines of code are excessively long.

````
<figure class="code">
<pre>
<code>
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
</code>
</pre>
<figcaption>
<span id="p51" class="page" epub:type="pagebreak" role="doc-pagebreak" aria-label="51">Page 51 &#8594;</span>
<p class="bqt">(Cayley 2002)</p>
</figcaption>
</figure>
````

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No |

### 1.18.3 Code Blocks with Line Numbers

There may be instances where code blocks are long or an author refers to specific lines of code in the surrounding text. There also may be a desire to allow readers to copy and paste code blocks without line numbers included in the copied text. To do so one will need to divert
from semantic encoding, and use CSS-only to include line numbers. Apply a CSS attribute which utilizes CSS line counting to provide line numbers automatically.

````
<figure class="code-linenumbers">
<figcaption>
<a data-locator="p157" class="page"></a>Practice Script 5.3: Revised simple statement combination
</figcaption>
<pre>
<span>myVariable = true;</span>
<span>if (myVariable == true) {</span>
<span> "The value of myVariable is TRUE";</span>
<span>} else {</span>
<span> "The value of myVariable is FALSE";</span>
<span>}</span>
</pre>
</figure>
````

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No |

### 1.18.4 Code Blocks with Line Numbers as Tables

In cases where code does not need to be copied and pasted but the display of line numbers is desirable, it is acceptable to encode the block of code as a table. For historical references to code this may be the most desirable, where excerpts of code are only needed to be displayed and line numbers start not a 1, but 3977, for example.

````
<table class="code">
<thead>
<tr>
<th class="th" colspan="2"><a data-locator="p10"
class="page"></a>Table 1.1. Excerpt from Heartbleed patch
(t1\_lib.c) by snhenson et al. (2015)</th>
</tr>
<tr>
<th class="tch">Line</th>
<th class="tch">Code</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<pre><code>3977</code></pre>
</td>
<td>
<pre>
<code>/* Read type and payload length first */</code>
</pre>
</td>
</tr>
<tr>
<td>
<pre><code>3978</code></pre>
</td>
<td>
<pre>
<code>if (1 + 2 + 16 &#x3e; s-&#x3e;s3-&#x3e;rrec.length)</code>
</pre>
</td>
</tr>
</tbody>
</table>
````

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No |

### 1.18.5 Comparing Code Blocks with Line Numbers

In other cases, two different blocks of code may need to be compared to one another side-by-side, along with the display of line numbers. In this case the code blocks should be encoded in a table, and follow the general pattern in 1.18.4. Note that in this case an additional CSS attribute is applied to the table element.

````
<table class="code compare">
<thead>
<tr>
<th class="th" colspan="3"><a data-locator="p59"
class="page"></a>Table 2.3. Two example FizzBuzz loops in
Ruby</th>
</tr>
<tr>
<th class="tch" style="width: 10%;">Line</th>
<th class="tch">Example 2.3.a</th>
<th class="tch">Example 2.3.b</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<pre><code>1</code></pre>
</td>
<td>
<pre>
<code>for i in 1..100</code>
</pre>
</td>
<td>
<pre>
<code>100.times do |i|</code>
</pre>
</td>
</tr>
<tr>
<td>
<pre><code>2</code></pre>
</td>
<td>
<pre>
<code> if i%3 == 0 then</code>
</pre>
</td>
<td>
<pre>
<code> i = i+1</code>
</pre>
</td>
</tr>
</tbody>
</table>
````

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No |

## 1.19 Footnotes and Endnotes

In general, the footnotes and endnotes are highly recommended to place at logical break of the book such as end of the chapter or end of the book, which will help the screen reader users to read the primary text.

Footnote and endnotes should be double-linked, allowing readers to navigate to a footnote or endnote section and back to the primary text.

### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No |

### 1.19.1 Footnotes in the body

````
<p>
In that year<a href="\#ft2f" role="doc-noteref" epub:type="noteref">2</a>
there were 67 mills engaged in the manufacture of cotton goods ...
</p>
<aside id="ft2f" role="doc-footnote" epub:type="footnote">
<p>
2 The manufacturing statistics for 1900 which follow are not those given in the Twelfth Census, but are taken from the <em>Census of Manufactures</em> ...
</p>
</aside>
<p>...</p>
````

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No |

### 1.19.2 Endnote section

The HTML Model allows for lists to contain headings, paragraphs, images, tables, etc. This means that applying list tagging can accommodate Endnote structures following `<ol>`.

If it is necessary to match the presentation of the text for editorial reasons, then it is suggested to use an unordered list tagging so that each endnote item is encapsulated as a list item.

A cluster of paras with `<p class="xxxxx">` tagging does not afford the same flexibility as list encoding, nor provide precision for isolating start and end of notes.

Note that `doc-endnote` role is used to identify the section containing the endnotes, and no role is required on the specific endnote when using an ordered list to organize endnotes.

````
<section epub:type="endnotes" role="doc-endnotes">
	<h2>Notes</h2>
	<ol role="list">
		<li role="listitem" class="endnote" epub:type="endnote" id="en172">
			<p class="en"><a role="doc-backlink" class="ennum" href="LucasPruett-0021.xhtml#en172r">1</a>.  The 2016 annual meeting of the American Musicological Society included a panel discussion entitled “Sexual Violence on Stage,” later published as a colloquy in the <i>Journal of the American Musicological Society</i> 71, no. 1 (2018): 213–53. Operas discussed included Mozart’s <i>Don Giovanni</i>, Floyd’s <i>Susannah</i>, Monteverdi’s <span lang="it" xml:lang="it"><i>L’Arianna</i></span>, Britten’s <i>The Rape of Lucretia</i>, Mazzoli’s <i>Breaking the Waves,</i> and Sankaram’s <i>Thumbprint</i>.
			</p>  
        </li>
		...
	</ol>
</section>
````

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No |

### 1.19.3 Back-linking notes
Providing links back to the primary text from the endnote or footnote section help readers navigate to and from notes. 

In this example a class `none` is applied to the `<ol>` to prevent automatic numbering, and the `doc-backlink` anchor is applied to a the number in the note.

````
<ol class="none">  
	<li><p epub:type="footnote" role="doc-footnote" id="p_3"><a role="doc-backlink" href="07_Preface.xhtml#not_1" id="pre_fn1">1</a>. Karla Jay, <i>Tales of a Lavender Menace: A Memoir of Liberation</i> (New York: Basic Books, 2000), 143.</p></li>
	...
</ol>
````

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No |


## 1.20 Bibliographies
Bibliographies should be structured using sections and lists to simplify access to the references.

```
<section role="doc-bibliography">  
	<h3 id="eh0602" class="eh">Works Cited</h3>  
    <ol role="list" class="references">  
	    <li class="rf" role="listitem">Afzal-Khan, Fawzia. “The Politics of Pity and the Individual Heroine Syndrome: Mukhtaran Mai and Malala Yousafzai of Pakistan.” <i>Performing Islam</i> 4, no. 2 (2015): 151–71.</li>  
	    <li class="rf" role="listitem">Baranello, Micaela. “When Cries of Rape are Heard in Opera Halls.” <i>New York Times</i>, July 16, 2015.</li>
	    ...
	</ol>
</section>    
```

### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No |

## 1.21 Indexes
Indexes should be structured using sections and lists to simplify access to the subjects.

```
<section id="index" class="chapter" aria-labelledby="headerindex01" epub:type="index" role="doc-index">      
	<header id="headerindex01">
		<h1 class="ctbm">Index</h1>      
	</header>      
	<ul class="index list-unstyled">
		<li id="in001" class="inf"><i>1619 Project</i>. <i>See</i> <a class="xref" href="LucasPruett-0033.xhtml#in163">Hannah-Jones, Nikole</a></li>
		<li id="in002" class="in"><i>20 Feet from Stardom</i> (documentary), <a class="xref" href="LucasPruett-0017.xhtml#p47">47</a></li>        
		...
	</ul>
</section>
```

### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No |

## 1.22 Content Numbering
Page numbers should be applied for titles that have a print equivalent. For titles that are digital-only and do not have a print equivalent, paragraph numbers should be applied.

### 1.22.1 Page Break Numbering
It is the Fulcrum practice to display page numbers in the flow of text. Other publishers may choose to visually hide the page numbers within the flow of text.

**Example coding that displays page numbers:**
````
<span id="p1" class="page" role="doc-pagebreak" aria-labelledby="pg1"></span>
<span id="pg1" aria-hidden="true" class="page">Page 1 &\#8594;</span>
````
In the above example, to avoid assistive technology reading the page number twice, the `aria-labelledby` is exposed to assistive technology while the visible page number element below is hidden from assistive technology. 

**Example coding that visually hides page numbers:**
````
<span id="p1" class="page" role="doc-pagebreak" aria-label="1"></span>
````

**NOTE:** When page breaks occur around headings (such as the start of a Part or Chapter), page breaks should always appear before the heading element and never inside of the heading element.
#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No, but strongly recommended |


### 1.22.2 Paragraph Numbering

Paragraph numbering requires adding a `class` identifier and `id` value to a `<p>`. Paragraph numbers should only be applied to elements that are true paragraphs, not elements that use the paragraph element for styling.

````
<p class="numberedpara" id="para11" title="Para11"/>
````

#### Required For
| U-M Vendor | Fulcrum Partner |
| ----------------- | ------------|
| Yes | No, but strongly recommended |

### 1.22.3 Line Numbering

Line numbering, such as in poems or code blocks, requires adding a `class` identifier and `id` value to a `<p>`.
````
<p class="numberedline" id="line11" title="Line11"/>
````

#### Required For
| U-M Vendor | Fulcrum Partner              |
| ---------- | ---------------------------- |
| No         | No, but strongly recommended |

## 1.23 Chapters split into multiple XHTML files

When chapters contain a large number of media and the total file size exceeds 10MB, then consider splitting the chapter into a series of HTML files. This will create smaller files for faster download and rendering within the Fulcrum EPUB Reading System. 

Inside each HTML file, please include `<meta content="chapter2" name="chapter2a" role="section"/>` updated by section to represent relationships between all files for a chapter. 

The reason for the metadata inclusion is to provide information so that Fulcrum is able to parse files to allow only chapters to display.

````
<html xmlns="http://www.w3.org/1999/xhtml"
      xmlns:epub="http://www.idpf.org/2007/ops" xml:lang="eng">
<head>
<title>More</title>
<link rel="stylesheet" href="../Styles/stylesheet.css" type="text/css"/>
<meta name="viewport" content="initial-scale=1.0;maximum-scale=5.0"/>
<meta content="chapter2" name="chapter2a" role="section"/>
</head>
<body>
<div>
<h3 class="subhead" id="sub4"><em>The Mid-Republican Period: The House</em></h3>
````

### Required For
| U-M Vendor | Fulcrum Partner              |
| ---------- | ---------------------------- |
| No         | No, but strongly recommended |

## 1.24 CSS Stylesheet

### 1.24.1 Standard CSS Stylesheets

The Fulcrum EPUB Specification provides three different CSS files for use in EPUBs. If possible, use one of the following standard CSS files in your EPUB, depending on its conversion process:

- [fulcrum.css](https://github.com/mlibrary/fulcrum-epub-spec/blob/master/fulcrum.css)
	- A generic CSS file for use in Fulcrum EPUBs
- [newgen.css](https://github.com/mlibrary/fulcrum-epub-spec/blob/master/newgen.css)
	- A CSS file for EPUBs produced by NewGen, adapting Fulcrum styles to NewGen conversion classes.
- [scribe.css](https://github.com/mlibrary/fulcrum-epub-spec/blob/master/scribe.css)
	- A CSS file for EPUBs produced through the Scribe Digital Hub, adapting Fulcrum styles to Scribe's conversion classes.

Unique styles per book can be added as needed as additional styles at the bottom of these CSS files. If styles are added or an external stylesheet is included, [validate the CSS](https://www.css-validator.org/).

#### Required For
| U-M Vendor | Fulcrum Partner |
| ---------- | --------------- |
| Yes        | No              |

### 1.24.2 CSS Units

- Font-size should always be defined in [relative units](https://kb.daisy.org/publishing/docs/wcag/resize-text.html).
- Do not use fixed values (`mm`, `cm`, `in`, `pt`, or `pc`) in CSS file.
- Do not use absolute-size values (`xx-small` - `xxx-large`) in CSS file.
- Control the `font-style` over the CSS whenever possible and avoid inline styles.

#### Required For
| U-M Vendor | Fulcrum Partner |
| ---------- | --------------- |
| Yes        | No              |

### 1.24.3 Colors

Ensure sufficient contrast so that text is legible, links are distinguishable from text, and do not rely on color to impart information, as not all users will be able to see the colors or perceive the differences. For example, if the color of a text provides a meaning to the content, then there should be some alternate method to convey the information to an assistive technology user. When unsure, check contrast using [WebAIM's Contrast Checker](https://webaim.org/resources/contrastchecker/).

#### Required For
| U-M Vendor | Fulcrum Partner              |
| ---------- | ---------------------------- |
| Yes        | No, but strongly recommended |

### 1.24.4 Background Images

If background images are to be included in the EPUB, setting the contrast between the background colors and images will help readers who have difficulty in distinguishing contrasts. Color contrast of 4:5:1 is the best practice followed in the industry.

#### Required For
| U-M Vendor | Fulcrum Partner              |
| ---------- | ---------------------------- |
| Yes        | No, but strongly recommended |

### 1.24.5 Hidden Content

There should not be any hidden content available in the EPUB files.

#### Required For
| U-M Vendor | Fulcrum Partner              |
| ---------- | ---------------------------- |
| Yes        | No, but strongly recommended |

### 1.24.6 CSS Property Reference

EPUB 3 user agents that visually render content may provide support for the CSS properties listed below, but inclusion is optional. Properties not listed may still be used (e.g., from evolving CSS 3 modules), but content authors should use due diligence and assess the impact on rendering and accessibility when using such properties.

Please refer to the [DAISY Accessible Publishing Knowledge Base](https://kb.daisy.org/publishing/docs/css/reference.html) for the most up to date CSS 2.1 properties allowed in EPUB.

#### Not Recommended Classes

<table border="1">
<thead>
<tr>
<th>Property</th>
<th>Considerations</th>
</tr>
</thead>
<tbody>
<tr>
<td style="vertical-align:top">
<p>
<a href="http://www.w3.org/TR/CSS21/visufx.html#propdef-clip">clip</a>
</p>
</td>
<td style="vertical-align:top"><ul>
<li><p>Although clipping content to 1 pixel is sometimes used on the
Web to hide content, support for the property and its reliance on
absolute positioning makes the practice not recommended in EPUBs.</p
></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top">
<p>
<a href="http://www.w3.org/TR/CSS21/generate.html#propdef-content">content</a>
</p>
</td>
<td style="vertical-align:top"><ul>
<li><p>Any content inserted using this property should be purely presentational,
as it typically won't be available to assistive technologies.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top"><p>direction</p></td>
<td style="vertical-align:top"><ul>
<li><p>The direction property is not supported in EPUB 3. HTML5 markup,
such as the <a href="http://www.w3.org/TR/html/text-level -semantics.html#the-bdi-element">bdi</a> and <a href="http://www.w3.org/TR/html/text-level -semantics.html#the-bdo-element"
>bdo</a> elements and <a href="http://www.w3.org/TR/html/dom.html#the-dir-attribute">dir</a> attribute, should be used to express directionality.</p></li>
</ul></td>
</tr>
<tr>
<td style="vertical-align:top">
<p>
<a href="http://www.w3.org/TR/CSS21/box.html#propdef-margin">margin</a>
</p>
<p>
<a href="http://www.w3.org/TR/CSS21/box.html#propdef-margin-top">margin-top</a>
</p>
<p>
<a href="http://www.w3.org/TR/CSS21/box.html#propdef-margin-right">margin-right</a>
</p>
<p>
<a href="http://www.w3.org/TR/CSS21/box.html#propdef-margin-bottom">margin-bottom</a>
</p>
<p>
<a href="http://www.w3.org/TR/CSS21/box.html#propdef-margin-left">margin-left</a>
</p>
</td>
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
<td style="vertical-align:top">
<p>
<a href="http://www.w3.org/TR/CSS21/visufx.html#propdef-visibility">visibility</a>
</p>
</td>
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
<li><p>Properties from the <a href="http://www.w3.org/TR/CSS21/aural.html">CSS 2.1 Aural style sheets
informative  appendix</a> should not be used in EPUB 3. The 'aural'
media type was deprecated by the same appendix, and the <a href="http://kb.daisy.org/publishing/docs/css/reference.html#css3speech">CSS 3 Speech module</a> defines the properties for the new 'speech'
type.</p></li>
</ul></td>
</tr>
</tbody>
</table>

#### Required For
| U-M Vendor | Fulcrum Partner              |
| ---------- | ---------------------------- |
| Yes        | No, but strongly recommended |

### 1.24.7 CSS 2.1 Pseudo-Classes
Please refer to the [DAISY Accessible Publishing Knowledge Base for the most up to date pseudo-classes](https://kb.daisy.org/publishing/docs/css/reference.html#css21classes) allowed in EPUB.

#### Required For
| U-M Vendor | Fulcrum Partner              |
| ---------- | ---------------------------- |
| Yes        | No, but strongly recommended |

### 1.24.8 CSS 2.1 Pseudo-Elements
Please refer to the [DAISY Accessible Publishing Knowledge Base for the most up to date pseudo-elements](https://kb.daisy.org/publishing/docs/css/reference.html#css21elements) allowed in EPUB.

#### Required For
| U-M Vendor | Fulcrum Partner              |
| ---------- | ---------------------------- |
| Yes        | No, but strongly recommended |

## 1.25 Fonts

If the input EPUB file contains fonts, then retain them in the output EPUB3 files. For web-ready PDF input files, do not embed fonts, unless otherwise requested by customer.

#### Required For
| U-M Vendor | Fulcrum Partner |
| ---------- | --------------- |
| Yes        | No              |

## 1.26 Formatting

Retain as much as possible of the formatting of the source EPUB and PDF files in the output EPUB3 file.

#### Required For
| U-M Vendor | Fulcrum Partner |
| ---------- | --------------- |
| Yes        | No              |

## 1.27 Boxed Text

Treat as text + images in reading order.

#### Required For
| U-M Vendor | Fulcrum Partner |
| ---------- | --------------- |
| Yes        | No              |

## 1.28 Marginalia and Sidebars

Treat as text + images in reading order.

#### Required For
| U-M Vendor | Fulcrum Partner |
| ---------- | --------------- |
| Yes        | No              |

## 1.29 Reading Order

Retain the reading order of the EPUB source files in the EPUB3 output. For the PDF source files, then match the source reading order in the EPUB3 output.

#### Required For
| U-M Vendor | Fulcrum Partner |
| ---------- | --------------- |
| Yes        | No              |

## 1.30 DPUB ARIA Semantics

Apply DPUB-ARIA semantic attributes according to the type of content.

Refer to the [DAISY Accessible Publishing Knowledge Base DPUB-ARIA guidelines](https://kb.daisy.org/publishing/docs/html/dpub-aria/index.html) for the most up to date list of roles, explanations, and code examples.

#### Required For
| U-M Vendor | Fulcrum Partner |
| ---------- | --------------- |
| Yes        | No              |

## 1.31 Accessibility

While much of the guidance in the Fulcrum EPUB Specification is aimed at ensuring an accessible EPUB3 file, in general applying the following points will help make the output accessible.

-   Image should be provided with alt text (if provided by customer) and decorative images should be left blank.

-   All the elements should be marked with [appropriate HTML tags](https://kb.daisy.org/publishing/docs/html/). 

-   Color contrast should be 4.5:1 which can be checked through ACE EPUB accessibility checker.

-   Zoom the text to 200% and ensure that the EPUB file remains readable without any text cut issues..

-   Text should not be captured as image.

-   Each HTML page should have proper title and the title should reflect the page title.

-   Language of the page should be defined and any other language text inside the content should be defined with proper language code.

#### Required For
| U-M Vendor | Fulcrum Partner              |
| ---------- | ---------------------------- |
| Yes        | No, but strongly recommended |

## Revision History

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
<tr class="even">
<td>2.2</td>
<td>May 14, 2019</td>
<td>HELIO-2661</td>
<td>tbelc@umich.edu</td>
</tr>
<tr class="odd">
<td>2.3</td>
<td>Jan. 15, 2020</td>
<td>HELIO-3146</td>
<td>tbelc@umich.edu</td>
</tr>
<tr class="even">
<td>2.4</td>
<td>April 15, 2020</td>
<td>HELIO-2651</td>
<td>tbelc@umich.edu</td>
</tr>
<tr class="odd">
<td>2.5</td>
<td>June 9, 2021</td>
<td>Clarify use of page numbering and paragraph numbering</td>
<td>J McGlone</td>
</tr>
<tr class="even">
<td>2.6</td>
<td>November 10, 2021</td>
<td>FULCRUMOPS-33</td>
<td>tbelc@umich.edu</td>
</tr>
<tr class="odd">
<td>3.0</td>
<td>March 2025</td>
<td>FULCRUMOPS-234 - indicate what is recommended vs. required and for whom; updates to extended description best practices; additional updates to match accessibility requirements; changes to EPUB specification; support for YouTube embeds; and more</td>
<td>J McGlone and T Belch</td>
</tr>
</tbody>
</table>

