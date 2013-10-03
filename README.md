JATS-Con paper, 2013
====================

To preview this, use the JATSPreviewStylesheets, which depends on you're being able
to run XSLT2 transformations.  The instructions below assume this is set up with the
alias `saxon9`.

```
# Get the DTD
wget ftp://ftp.ncbi.nlm.nih.gov/pub/jats/articleauthoring/1.0/jats-articleauthoring-dtd-1.0.zip
unzip -d dtd jats-articleauthoring-dtd-1.0.zip

# Get this paper
git clone https://github.com/Klortho/InconsistentXml.git

# Get the JATS preview stylesheets
git clone https://github.com/NCBITools/JATSPreviewStylesheets.git

# Transform!  Result is in JatsCon2013.html, which you can re-commit, if you want.
cd InconsistentXml
saxon9 -s:JatsCon2013.xml -o:JatsCon2013.html \
  -xsl:../JATSPreviewStylesheets/xslt/main/jats-html.xsl
```
