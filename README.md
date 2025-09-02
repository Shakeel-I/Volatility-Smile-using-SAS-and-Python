# Volatility-Smile-using-SAS-and-Python

ods graphics / reset width=6.4in height=4.8in imagemap;

proc sgplot data=AAPL;
	title height=14pt "Volatility Smile - AAPL Options";
	loess x=strike y=impliedVolatility / nomarkers;
	scatter x=strike y=impliedVolatility /;
	xaxis grid;
	yaxis grid;
run;

ods graphics / reset;
title;
