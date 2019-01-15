
---
title: 
author: Stefano Bussolon
description: 
comments: true
date: 
layout: post
slug: 
categories:
- categoria
tags:
- tag


build: | 
 pandoc -f markdown \
 /home/bussolon/documenti/didattica/r_dottorato/r_intro/dispensa/why_r.md \
 -o /home/bussolon/documenti/didattica/r_dottorato/tmp/why_r.html
 
 pandoc --filter pandoc-citeproc \
 -f markdown --toc \
 --latex-engine=xelatex \
 --variable=geometry:margin=0.5in --variable=geometry:paperheight=19.71cm --variable=geometry:paperwidth=14.78cm \
 --biblio=/home/bussolon/documenti/ricerca/bibliografia/hci/bibliografia.bib \
 --csl=/home/bussolon/documenti/ricerca/bibliografia/hci/chicago-author-date.csl \
 .md \
 -o 
 --self-contained -t docx

...

# Perché r

[Introduction - Advanced R.](http://adv-r.had.co.nz/Introduction.html)

## Perché R?

Perché è gratuito, open source, disponibile su più sistemi operativi (windows, mac, linux). replicabilità
Perché dispone di una enorme catalogo di pacchetti per l'importazione di dati, la loro manipolazione, l'analisi statistica, la visualizzazione, la creazione di report, e per elaborazioni più complesse (ad esempio machine learning).
Questi pacchetti sono spesso molto aggiornati, e rappresentano lo stato dell'arte nell'analisi dei dati.

Il linguaggio è stato specificamente creato e sviluppato per l'analisi dei dati.

Internet è ricco di risorse, anche gratuite, che permettono di imparare ad usare R.

Per i più esperti, R offre anche delle caratteristiche avanzate: programmazine funzionale, possibilità di invocare funzioni in altri linguaggi (c, fortran).

R è estensibile, attraverso l'installazione di pacchetti esterni.
In ambito statistico e in psicometria R è sostanzialmente uno standard


## R vs excel

Excel funziona meglio su cose semplici e che non ho bisogno di replicare.

Quando è necessario fare delle analisi statistiche più complesse, integrare insiemi di dati, creare presentazioni grafiche, è decisamente meglio R.

## Vantaggi di R


* R ha l'ecosistema più ricco ed avanzato di pacchetti per l'analisi dei dati. Dietro ad R c'è una grossa comunità di utilizzatori che condivide pacchetti, librerie e che è disponibile ad aiutare, attraverso forum e spazi di collaborazione
* R offre strumenti di visualizzazione più avanzati
* R è gratuito ed open source
* R è un linguaggio di programmazione.
* R riesce a leggere (importare) una vasta gamma di dati
* R può manipolare file di dati molto grandi
* negli insiemi di dati più grandi, R è più veloce
* con R è possibile organizzare meglio i progetti (separando ed integrando dati, codice/script, testi, figure)
* è molto più facile automatizzare i processi con R che con excel. Più in generale, è più facile automatizzare un processo in un ambiente di programmazione che con una GUI.
* accuratezza: excel è meno accurato, e più soggetto a bug, rispetto ad R.
Gli script in R

* sono più facili da documentare
* possono essere ri-utilizzati
* è più facile replicare una analisi
* possono essere utilizzati su basi di dati diverse
* se il codice viene commentato, è più facile ricordare cosa si sta facendo (o capire cosa ha fatto chi ha scritto il codice). Documentare i passaggi fatti con excel è molto meno naturale.

Riproducibilità: è molto più facile riprodurre analisi anche complesse. Questo ha almeno due vantaggi:

* è possibile applicare, in maniera piuttosto semplice, la stessa analisi su dati diversi
* questo rende più facile la verifica e la riproducibilità delle analisi, ad esempio da parte di ricercatori o laboratori diversi (open science?)
* è possibile applicare al codice dei software di controllo di versione (ad esempio git)
* è facile condividere il proprio codice, ed adottare delle metodologie di collaborazione


### Riferimenti

* [Excel vs R: When to use what - R for Excel Users](https://www.rforexcelusers.com/excel-vs-r-when-to-use-what/) 
* [R for beginners: How to transition from Excel to R | TrendCT](https://trendct.org/2015/06/12/r-for-beginners-how-to-transition-from-excel-to-r/)
Come fare le stesse cose con Excel e con R:

* aprire un file
* conoscere il numero di righe e colonne
* dare un occhio ai dati
* analizzare la struttura dei dati
* selezionare i dati per cella, riga, colonna
* modificare il formato di una colonna
* ordinare un dataframe
* creare una formula
* filtrare le righe in base ai valori di una colonna
* fare calcoli sulle colonne
* fare delle tabelle *pivot*

Interessante anche [R for Excel Users - Alteryx Community](https://community.alteryx.com/t5/Data-Science-Blog/R-for-Excel-Users/ba-p/138441)
* [Understanding R programming over Excel for Data Analysis | gap intelligence](https://gapintelligence.com/blog/2016/understanding-r-programming-over-excel-for-data-analysis)
* [Why would you learn R if you have Excel working well? - Quora](https://www.quora.com/Why-would-you-learn-R-if-you-have-Excel-working-well)



## R vs Python

Se excel non è la soluzione migliore per fare analisi dei dati, R non è l'unico ambiente disponibile. Fra le alternative, una delle più accreditate è il linguaggio di programmazione python, integrato con alcuni pacchetti quali pandas e numpy.

Il dibattito Python vs R è molto acceso, in quanto entrambi i linguaggi costituiscono un'ottima scelta.

L'opinione più condivisa è che nella statistica inferenziale, R *batte* Python. Nella manipolazione dei dati i due ambienti se la cavano altrettanto bene. Python ha il vantaggio di essere un linguaggio di programmazione *all purpose*, mentre R è molto più specializzato all'analisi dei dati.

## Approccio pragmatico

***TODO*** 

approccio haker?


### Riferimenti

* [Python vs R for Data Science](https://medium.com/@data_driven/python-vs-r-for-data-science-and-the-winner-is-3ebb1a968197)
* [R Vs Python: What's the difference?](https://www.guru99.com/r-vs-python.html)
* [Python or R for Machine Learning and Data Science | Netguru Blog on Python](https://www.netguru.co/blog/python-or-r-for-machine-learning-and-data-science)
* [Choosing R or Python for data analysis? An infographic (article) - DataCamp](https://www.datacamp.com/community/tutorials/r-or-python-for-data-analysis)
* [Python vs. R : statistics](https://www.reddit.com/r/statistics/comments/8v4zp4/python_vs_r/)




