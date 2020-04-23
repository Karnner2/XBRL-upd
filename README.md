# XBRL-upd
An updated CRAN-based XBRL package to integrate with finstr-upd (Forked from Bergnant/Finstr)
Update corrects the http/https error that XBRL suffers from. Adjustment was suggested by a rather unknown user at StackExchange.

I became tired editing the source everytime I closed my R-sessions or switched projects and the issue became particularly troublesome when I began integrating XBRL into Sweave/Knitr situations because they compile under independent global environments. 

I have taken the source from XBRL and from Finstr (forked from Bergnant/finstr) and made adjustments so that the packages will work stand-alone with the current SEC-EDGAR adjustments for XML/XBRL data files. 

## Uses in International XBRL
Testing shows that the extraction will work generally with any XBRL taxonomy including sourced from Companies House UK, Edinet (Japan), Shanghai and Shenzen exchanges (China), and SEDGAR (Canada). I believe the Taxonomy extraction will work with any XBRL financial report/statement set but I have not tested them all. 

Be aware that if you are pulling from a directory that is not as well formed as the SEC-EDGAR, you may need to download the XML file for the firm (likely a zip), and place it on your local computer. 

Use the low-level or high-level functions built into XBRL to extract the components manually. The xbrl.vars values can be passed into xbrl_get_statements from finstr directly after that. I did this to parse the Japanese financial statements as finstr would do for US based firms. The caveat is that you, of course, need to read the local language (e.g. Japanese kanji, **etc.**). 
