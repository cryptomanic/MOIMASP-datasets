## Dataset A  
It consists of 6 transactions of 5 items each.    
Number of unique items are 8.   
They are 1 2 3 4 5 7 8 9.    

Dataset `B`, `C`, `D` and `E` are generated randomly using the below `R` script.  

```
generate.data.mod <- function(nrow, ncol, rng) {
  data <- matrix(nrow = nrow, ncol = ncol) 
  for(i in 1:nrow) {
    data[i, ] <- sample(1:rng, ncol)
  }
  old_data <- as.data.frame(data)
  new_data <- data
  new_data[1, 1] <- as.character(new_data[1, 1])
  
  list(old_data = old_data, new_data = new_data)
}

set.seed(10001)
B <- generate.data.mod(20, 20, 25)

set.seed(1010)
C <- generate.data.mod(40, 40, 47)

set.seed(1010)
D <- generate.data.mod(100, 100, 105)

set.seed(1010)
E <- generate.data.mod(1000, 1000, 1020)
```

## Dataset B  
It consists of 20 transactions of 20 items each.    
Number of unique items are 25.   
They are 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25

## Dataset C  
It consists of 40 transactions of 40 items each.    
Number of unique items are 47.   
They are 1 2 3 4 5 6 7 8 9 10 . . . . . . 45 46 47

## Dataset D  
It consists of 100 transactions of 100 items each.    
Number of unique items are 105.   
They are 1 2 3 4 5 6 7 8 9 10 11 12 . . . . . . 100 101 102 103 104 105

## Dataset E  
It consists of 1000 transactions of 1000 items each.    
Number of unique items are 1020.   
They are 1 2 3 4 5 6 7 8 9 10 11 12 . . . . . . 1015 1016 1017 1018 1019 1020
