JATS-Con paper, 2013
====================

To preview this, use the JATSPreviewStylesheets, which depends on you're being able
to run XSLT2 transformations.  The instructions below assume this is set up with the
alias `saxon9`.

```
# Get the DTD
wget ftp://ftp.ncbi.nlm.nih.gov/pub/jats/articleauthoring/1.0/jats-articleauthoring-dtd-1.0.zip
unzip -d dtd jats-articleauthoring-dtd-1.0.zip
git clone https://github.com/Klortho/InconsistentXml.git
git clone https://github.com/NCBITools/JATSPreviewStylesheets.git
cd InconsistentXml
cp ../JATSPreviewStylesheets/jats-preview.css .
saxon9 -s:JatsCon2013.xml -o:JatsCon2013.html \
  -xsl:../JATSPreviewStylesheets/xslt/main/jats-html.xsl
```
