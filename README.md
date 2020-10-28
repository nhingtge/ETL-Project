# Pauper Magic ETL
An ETL project to scrape Pauper tournament data and then deploy it to MongoDB

## Table of Contents
* [General Info](#general-info)
* [Technologies](#technologies)
* [Setup](#setup)
* [Sources](#sources)

## General Info
Magic the Gathering is a collectible card game in which players craft decks and play them against each other hoping to win by casting spells and attacking with creatures.
Within any format it is important to understand not just one's own deck but also the various decks one may encounter in order to better counter the opponent's strategy. 
As such, the need for good organized tournament data is massive. There are various formats one might play, but the Pauper format was chosen for its relative simplicity.
Decks are composed of a 60 card "main" and a 15 card "sideboard".  Mains must be played unaltered in game 1, and the cards in the sideboard may be substituted into
the main for games 2 and 3 in a best of 3 match. As such, the sideboard is usually filled with "hate" (cards which exist to disrupt a specific strategy). Limited slots
mean that sideboards must be filled very carefully to ensure narrow hate cards can hinder an opponent's strategy while also being usable in one's own. For this reason,
a database was crafted with particular attention towards ensuring data relevant to picking proper hate are preserved. To be precise, this means that color, typelines, and
"power" and "toughness" (the amount of damage a creature can deal in combat and the amount of damage needed to kill a creature) were emphasized. Data was collected by
scraping tournament data from a popular Magic the Gathering tournament website (mtggoldfish), and data about the cards in those decks were scraped from the official
Magic the Gathering "Oracle Text" (gatherer).

In order to assist anyone seeking to understand what a Pauper deck looks like, an example has been included in sources.
  
This project was done for a data visualization bootcamp with particular interest towards learning web-scraping.  

## Technologies
* Python version: 3.6.10.final.0
* Pandas version: 1.0.4
* Splinter
* BeautifulSoup
* Chromedriver
* MongoDB
* pymongo


## Setup
In order to rerun these programs, chromedriver must be installed and in the notebooks folder. Note that the exact version of chromedriver that can be used also depends on
which version of the Google Chrome browser is installed. Unfortunately, Chrome likes to run updates quietly in the background, so we suggest anyone attempting to rerun
any of these files simply update Chrome to the newest version and download the lastest chromedriver.


## Sources
https://www.mtggoldfish.com/metagame/pauper#paper  
https://gatherer.wizards.com/Pages/Default.aspx  
https://tappedout.net/mtg-decks/28-10-20-pauper-goblins/?cb=1603871247
