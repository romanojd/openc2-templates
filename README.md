# OpenC2 Document Workflow

OASIS policies state: 
> All approved versions of OASIS Deliverables must be published in (1) editable source, (2) HTML or XHTML, and (3) PDF formats. The TC must explicitly designate one of those formats as the authoritative document.

OpenC2 TC is using a markdown-formatted text file as its authoritative and "editable source". Markdown itself is easy to edit, focused more on content than format, and enables very strong version control. But markdown is not always the best for collaboration. Google Docs provides a multi-user, real-time, concurrent collaboration environment. In order to use the collaboration capabilities of Google, Google Docs documents need to be converted into a markdown-formatted text file.

A conversion script was developed to facilitate this. After all proposed changes have been accepted in the Google Document, the script will create a markdown file, which is the authoritive, editable source. The HTML document is easily converted into HTML by design. The paired-down formatting codes are designed to be completely represented by HTML. (Note: We are currently working with OASIS to develop a standard CSS to format the resultant HTML using OASIS developed style guidelines.) The PDF document can then be created from the HTML.

The workflow and the source code for the file conversions will be available to OASIS for any TC that wishes to use a Markdown-formatted text files as the authoritative, editable source.
