# DAX

```
IF(
  EXPR,TRUE,FALSE
)
```
```
CALENDARAUTO(
  <INT: START AFTER>
)

CALENDARAUTO(12)
```

```
ADDCOLUMNS(
  CALENDARAUTO(),
  "Year", YEAR([Date]),
  "Month", MONTH([Date]),
  "Month Name", FORMAT([Date],"MMM")
)

```

* Count Row
```
COUNTROWS(<table>
```
```
COUNT(<table>.<column>)
```



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

# AVERAGEX

```
AVERAGEX(table, table[col1] - table[col2]) // apply across the card 
```

# CALCULATE
```
CALCULATE(
  SUM(DF[COL1]),
  FILTER(DF,DF[COL2]=''),
  FILTER(DF, DF[COL3]='')
)
```
