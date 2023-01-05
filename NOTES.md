# Notes 

Quick notes to describe the process of converting the original Word document to TEI.

## Word to TEI

We generate two TEI conversions using two tools from the web:

* V1: [Alldocs](https://alldocs.app/convert-word-docx-to-tei-simple), Alldocs is a site that converts from and to various file formats, including DOC to TEI. Allodcs uses pandoc.
* V2: [OxGarage](https://oxgarage2.tei-c.org). OxGarage is a site created by the TEI consortium to and from various file formats, with an emphasis on TEI.

A helpful document for future work like this: http://www.dotporterdigital.org/workflow-ms-word-to-tei/ 

## Image Extraction

One problem with these conversions is that no images are extracted during the conversion. So,
we resort to [the method of converting DOC to a web page](https://support.microsoft.com/en-us/topic/wd-how-to-extract-embedded-images-from-a-word-document-f478bf7f-3bba-6afb-6ddc-3eeb284af36b), and then copying the exported images to a loca `media/` directory, which 
the above files assume to exist. Because the exported image filenames are zero-padded, but the references in the converted docs are not, we pad the zeros in the docs.

## Next Steps

* The schema of the exported files needs to be transformed to the Multepal schema.
* This will require analyzing the current schema and mapping elements to the target schema.