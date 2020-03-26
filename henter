# -*- coding: utf-8 -*-
import pandas as pd
import requests


csv_out = r"[Link til fuld sti]" #fuld sti til dokumentet der skal skrivs til i linje 15. inkl fil og format. 
url = r"https://netbank.totalkredit.dk/netbank/showStockExchange.do" # link til Totalkredits kurser.

r = requests.get(url)

data = r.text

tables = pd.read_html(r.text)[1] #ændres til 0 eller 1 alt efter om du ønsker med/uden afdrag
print(tables) #bare for at få noget på konsollen
tables.to_csv(csv_out,encoding = "utf-8") #eksporterer resultatet. Lav evt. header=False og mode='a' - for append.

