```Frequency
a = 14
c = 21
m = 53
x = 0
total_nums = 1000
random_numbers = c()
#Generate Random Numbers
for (i in 1:total_nums) {
  x <- (a * x + c) %% m
  random_numbers = c(random_numbers, x) 
}

count = 0
for (i in 1:53){
  for(j in random_numbers){
    if(j==i){
      count = count + 1
    }
  }
  cat('\n',i, 'frequency', count, 'and probalistic frequency is ', (count/total_nums) * 100 )
  count = 0
} 
