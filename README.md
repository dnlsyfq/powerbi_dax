# DAX

* Columns evaluates each row
* Measure aggregates multiple rows 

Profit margin ratio compares the total profit to the total sales

## Function
```
SUM(COL)
AVERAGE()
COUNT()
TODAY()
MONTH()
YEAR()
IF()
AND()
OR()
CONCATENATE()
UPPER()
LEFT('DATACAMP',4) // DATA
```

## Measures
```
MAX(table[COL])
```

## Calculate Function
```
CALCULATE(
  SUM(Commodities[Volume]),
  FILTER(Commodities,Commodities[Symbol]='Gold'),
  FILTER(Commodities,YEAR(Commodities[Date])=2021)
)
```
```

```

## Variable in PowerBI
```
VAR GoldVolume20 = CALCULATE(
  SUM(Commodities[Volume]),
  FILTER( Commodities, Commodities[Symbol]='Gold'),
  FILTER( Commodities, YEAR(Commodities[Date])=2020)
  )
  
RETURN DIVIDE([GoldVolume21]-GoldVolume20, GoldVolume20)
```

## Dates
```
YEAR(<date>
QUARTER(<datetime>)
MONTH(<datetime>)

FORMAT(<date>,<"dddd">) // Friday
FORMAT(<date>,<"h:nn:ss">)
CALENDAR(<start_date>,<end_date>) // table with single column date
CALENDARAUTO(<fiscal year end month>) // table with single column take earliest and latest date in the model e.g. CALENDARAUTO(12)
```
