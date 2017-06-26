# GreatFriends - TDD Exercises

## I. Day Grouping
Input is integer array 
and output is a string.

```
0. Input: []
  Output: ""

1. Input: null
  Output: ""

2. Input: [1]
  Output: "1"

3. Input: [1, 2, 3]
  Output: "1-3"

4. Input: [1, 2, 5]
  Output: "1-2 and 5"
 
5. Input: [1, 2, 5, 6, 7]
  Output: "1-2 and 5-7"

6. Input: [1, 3, 5]
  Output: "1, 3 and 5"

7. Input: [1, 6, 5]
  Output: "1 and 5-6"

8. Input: [1, 5, 5, 6, 7, 2, 15, 16, 17]  
  Output: "1-2 and 5-7 and 15-17"
 
9. Input: [0, 1]
  Output: Throws InvalidDayException

X. Input: [29, 30, 31, 32]
  Output: Throws InvalidDayException
```

## II. Car Fuel Consumption 

Calcuate fuel consumption rate per fill-up in Kilometers per Liter unit. Assume that all fill-ups are full tank.

### Fill-Up Records
| No | Odometer |  Liters   | Full? | KmL
| -- | -------- | --------- | ----- | ---
| 1  | 1000     |   50.00   | Yes   | 
| 2  | 1600     |   60.00   | Yes   | 
| 3  | 2200     |   50.00   | Yes   | 
| 4  | 2600     |   54.98   | Yes   | 

### Fillups.csv - Fill-Up Records in CSV
```
No,Date,Odometer,Liters,IsFull,KmL
1,2017-01-01,35000,52.991,True,8.41
2,2017-01-07,35422,50.182,True,9.02
3,2017-01-12,36003,64.444,True,9.15
4,2017-01-14,36395,42.833,True
```

Uses [CsvHelper](https://joshclose.github.io/CsvHelper/) 
to read `FillUps.csv` file into strongly-typed list (`List<FillUpData>`).
Install CsvHelper via [NuGet](https://www.nuget.org/packages/CsvHelper/3.0.0-chi05)
```
  public class FillUpData {
    public int No { get; set; }
    public DateTime Date { get; set; }
    public int Odometer { get; set; }
    public double Liters { get; set; }
    public bool IsFull { get; set; }
    public double? KmL { get; set; }
  }
```

## III. Online Shop with Partners

1. All partners must be added to main shop.
![image](https://user-images.githubusercontent.com/344784/27511065-532d98a8-5947-11e7-89b9-19e92a551a93.png)

2. `Partner A` can be added to `Partner B` so that all products in `Partner A` also displays in `Partner B`'s website.
![image](https://user-images.githubusercontent.com/344784/27511192-308f0a5a-5949-11e7-91e1-32d981cee42e.png)
Example: Partner-3 is added to Partner-1

3. Partner can be added in two-way direction.

![image](https://user-images.githubusercontent.com/344784/27511204-6899a180-5949-11e7-9532-7bf7b4747353.png)


