# Volatility-Smile-using-SAS-and-Python
<img width="495" height="371" alt="image" src="https://github.com/user-attachments/assets/c0a32a23-4b6d-443e-be3d-e8285e7ecfec" />






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
