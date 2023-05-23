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
