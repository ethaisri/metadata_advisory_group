# TriCo Print Monograph Copy Cataloging

* [Search Millennium for matching bibliographic record](https://github.com/ethaisri/metadata_advisory_group/blob/master/print_monograph_copy_cataloging.md#search-millennium-for-matching-bibliographic-record)  
* [Edit the bibliographic record](https://github.com/ethaisri/metadata_advisory_group/blob/master/print_monograph_copy_cataloging.md#edit-the-bibliographic-record)
  * [Millennium fixed fields](https://github.com/ethaisri/metadata_advisory_group/blob/master/print_monograph_copy_cataloging.md#millennium-fixed-fields)  
  * [MARC fixed fields](https://github.com/ethaisri/metadata_advisory_group/blob/master/print_monograph_copy_cataloging.md#marc-fixed-fields)  
  * [MARC variable fields](https://github.com/ethaisri/metadata_advisory_group/blob/master/print_monograph_copy_cataloging.md#marc-variable-fields)  
    * [001 - OCLC number](https://github.com/ethaisri/metadata_advisory_group/blob/master/print_monograph_copy_cataloging.md#001---oclc-number)  
    * [100 - Author (personal name)](https://github.com/ethaisri/metadata_advisory_group/blob/master/print_monograph_copy_cataloging.md#100---author-personal-name)  
    * [110 - Author (corporate name)](https://github.com/ethaisri/metadata_advisory_group/blob/master/print_monograph_copy_cataloging.md#110---author-corporate-name)  
    * [245 - Title statement](https://github.com/ethaisri/metadata_advisory_group/blob/master/print_monograph_copy_cataloging.md#245---title-statement)  
    * [250 - Edition statement](https://github.com/ethaisri/metadata_advisory_group/blob/master/print_monograph_copy_cataloging.md#250---edition-statement)  
    * [260/264 - Publication statement](https://github.com/ethaisri/metadata_advisory_group/blob/master/print_monograph_copy_cataloging.md#260264---publication-statement)  
    * [300 - Physical description](https://github.com/ethaisri/metadata_advisory_group/blob/master/print_monograph_copy_cataloging.md#300---physical-description)  
    * [33X - Content, media, and carrier types](https://github.com/ethaisri/metadata_advisory_group/blob/master/print_monograph_copy_cataloging.md#33x---content-media-and-carrier-types)  
    * [490/830 - Series statement](https://github.com/ethaisri/metadata_advisory_group/blob/master/print_monograph_copy_cataloging.md#490830---series-statement)  
    * [5XX - Notes](https://github.com/ethaisri/metadata_advisory_group/blob/master/print_monograph_copy_cataloging.md#5xx---notes)  
    * [6XX - Subject headings](https://github.com/ethaisri/metadata_advisory_group/blob/master/print_monograph_copy_cataloging.md#6xx---subject-headings)  
    * [7XX - Additional access points](https://github.com/ethaisri/metadata_advisory_group/blob/master/print_monograph_copy_cataloging.md#7xx---additional-access-points)  
    * [856 - URLs](https://github.com/ethaisri/metadata_advisory_group/blob/master/print_monograph_copy_cataloging.md#856---urls)  

## Search Millennium for matching bibliographic record
* Search for the book by ISBN.
* If the book does not have an ISBN, search for the book by title (omitting initial articles).
* Confirm that you have found a match by checking that the title found on the book’s title page matches the title found in the MARC 245 field; that the pagination found in subfield |a of the 300 field is correct; and that the publication/copyright date(s) found on the book’s title page or title page verso matches the date(s) found in the 260 or 264 field(s).
* If you have any trouble finding a match; if you think there might be duplicate bibliographic records; or if the bibliographic record is brief (see next bullet point), consult your supervisor.
* Signs that the bibliographic record is brief include:
  * There are no 050 or 090 fields.
  * The title in the 245 field is in all caps.
  * The 300 field is absent or incomplete.
  * There are no 33X fields.
  * There are no 6XX fields.

## Edit the bibliographic record
### Millennium fixed fields
* Fill in the CAT DATE field using the shortcut ``t``.
* Make sure that the MAT TYPE field is filled in with ``a BOOKS``.
* Make sure that the ATRTY field is filled in with ``g``.

### MARC fixed fields
* Check that the date matches the one found in subfield |c of the 260 or 264 field.
* Check that the [language code](http://www.loc.gov/marc/languages/language_code.html) is correct (``eng`` for English).

### MARC variable fields
#### 001 - OCLC number
* This field contains the OCLC number. The 035 field also contains the OCLC number in addition to other information. Occasionally vendor-supplied bibliographic records lack the 001 field. If that happens, create an 001 field and add to it the first number found in the 035 field.  
  ```
  001 __ 51939553
  035 __ (OCoLC)51939553
  ```
#### 100 - Author (personal name)
* This field contains the first named author in the statement of responsibility (subfield |c of the 245 field). Subsequently named authors may appear 7XX fields.
* Individuals who make a secondary contribution to a book (e.g., editors, illustrators, and translators) should appear in a 700 field instead of a 100 field.
  ```
  100 1_ Groth, Michael E.,|d1965-|eauthor
  100 1_ Austen, Jane,|d1775-1817
  ```
#### 110 - Author (corporate/conference name)
* This field is used if the main author is a corporate body/organization or a conference/meeting. 
  ```
  110 2_ Organisation for Economic Co-operation and Development
  ```
#### 245 - Title statement
* Check that the statement of responsibility matches the title page. 
* Check that the names mentioned in the statement of responsibility are present in 7XX fields or in a 1XX field plus 7XX fields. If any of the names present in the statement of responsibility do not appear in 1XX/7XX fields, refer.
#### 250 - Edition statement
* This field contains the edition of the book and may include a statement of responsibility in subfield |b.
  ```
  250 __ First illustrated edition.
  250 __ Complete and unabridged.
  250 __ 7th edition /|brevised by Lizzie Hexam.
  ```
#### 260/264 - Publication statement
* This field contains information about where, by whom, and when a book was published. In older records the publication statement appears in a 260 field. In newer records the publication statement appears in a 264 field with second indicator 1. In newer records the 264 field with second indicator 4 is used for the copyright date.
  ```
  260 __ Philadelphia, PA :|bPhiladelphia Yearly Meeting of the Religious Society of Friends,|c1997
  264 _1 Princeton, New Jersey :|bPrinceton University Press,|c2017
  264 _4 |c©2014
  ```
#### 300 - Physical description
* This field contains the pagination, illustrated content (if applicable), and physical dimensions of the book (recorded to the next whole centimeter up).
* For the physical dimension of the book, only the height of the book is recorded unless the width of the book is either less than half the height or greater than the height. In those cases the height x width is recorded. 
  ``` 
  300 __ xii, 256 pages, 10 pages of plates ;|c 23 cm
  300 __ 3 volumes :|billustrations ;|c27 cm
  300 __ 420 pages :|b color illustrations, 5 maps ;|c28 cm x 34 cm
  ```
#### 33X - Content, media, and carrier types
* Each bibliographic record must have the following 33X fields:
  ```
  336 __ text|btxt|2rdacontent
  337 __ unmediated|bn|2rdamedia
  338 __ volume|bnc|2rdacarrier
  ```
#### 490/830 - Series statement
* Proofread
#### 5XX - Notes
* Remove notes that only apply to a copy of a book that is held by a **non**-TriCo library.
* Retain notes that apply to a copy of a book that is held by a TriCo library.
* All TriCo local notes (found in the 590 field) must identify the the TriCo institution. TriCo institutions must have separate 590 fields.
* If the book is a translation, make sure there is a note in this field. Use the form "In [name_of_language] translated from the [name_of_language]."
  ```
  546 __ Translated from the French.
  ```
#### 6XX - Subject headings
* Each bibliographic record must have at least one subject heading.
* Do not alter or delete any subject headings that have a ``0`` in the second indicator.
* For 655 fields, do not alter or delete any subject headings that have ``lcgft`` in subfield l2.
* Delete non English-language headings.
* Delete headings that have ``bisach``, ``bisacmt``, or ``bisacrt`` in subfield |2.
#### 7XX - Additional access points
* Check for names listed in subfield |c of the 245 field.
  ```
  700 1_ Barnbaum, Deborah R.,|d1967-|eauthor
  710 2_ Light Work (Organization : Syracuse, N.Y.)
  ```
#### 856 - URLs
* If the field has a subfield |3 before any of the text, change the "3" to a "z".
* If there are multiple links to Table of Contents information, remove ones that are coming from non-English language sources in subfield |3.
* If the only Table of Contents link has ``Inhaltsverzeichnis`` in subfield |3, replace ``Inhaltsverzeichnis`` with ``Table of Contents``.
* Remove links to any licensed/proprietary content not applicable/accessible to any of the TriCo institutions.
* Remove links to cover images.

Save the changes that you made to the bibliographic record.
