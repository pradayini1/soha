number=1
rows=5
for((i=1; i<=rows; i++))
do
  for((j=1; j<=i; j++))
  do
    echo -n "$number "
    number=$((number + 1))
  done
  number=1
  echo
done

-----------------------------------------

#Bash Shell Script to print Floyd's Triangle
number=1
rows=4
for((i=1; i<=rows; i++))
do
  for((j=1; j<=i; j++))
  do
    echo -n "$number "
    number=$((number + 1))
  done
  echo
done

--------------------------------------------

#Bash Shell Script to print Floyd's Triangle
number=1
rows=4
for((i=1; i<=rows; i++))
do
  for((j=1; j<=i; j++))
  do
    echo -n "$number "
    number=$((number + 1))
  done
  echo
done
-----------------------------------
number=1
rows=5
for((i=1; i<=rows; i++))
do
  for((j=1; j<=i; j++))
  do
    echo -n "$number "
    number=$((number + 1))
  done
  number=1
  echo
done
------------------------------------------
14
------ascending order
arr=(10 8 20 100 12)

echo "Array in original order"
echo ${arr[*]}

# Performing Bubble sort 
for ((i = 0; i<5; i++))
do
    
    for((j = 0; j<5-i-1; j++))
    do
    
        if [ ${arr[j]} -gt ${arr[$((j+1))]} ]
        then
            # swap
            temp=${arr[j]}
            arr[$j]=${arr[$((j+1))]}  
            arr[$((j+1))]=$temp
        fi
    done
done

echo "Array in sorted order :"
echo ${arr[*]}
n=5
arr=(10 8 20 100 12) 

echo "Original array is: ${arr[*]}";

flag=1;
for (( i = 0; i < $n-1; i++ ))
do
    flag=0;
    for ((j = 0; j < $n-1-$i; j++ ))
    do
        if [[ ${arr[$j]} -gt ${arr[$j+1]} ]]
        then
            temp=${arr[$j]};
            arr[$j]=${arr[$j+1]};
            arr[$j+1]=$temp;
            flag=1;
        fi
    done

    if [[ $flag -eq 0 ]]; then
          break;
    fi
------Descending oredr

#!/bin/bash
echo "enter maximum number"
read n
# taking input from user
echo "enter  Numbers in array:"
for (( i = 0; i < $n; i++ ))
do
read nos[$i]
done
#printing the number before sorting
echo "  Numbers in an array are:"
for (( i = 0; i < $n; i++ ))
do
echo ${nos[$i]}
done
# Now do the Sorting of numbers
for (( i = 0; i < $n ; i++ ))
do
for (( j = $i; j < $n; j++ ))
do
if [ ${nos[$i]} -lt ${nos[$j]}  ]; then
t=${nos[$i]}
nos[$i]=${nos[$j]}
nos[$j]=$t
fi
done
done
# Printing the sorted number in descending order
echo -e "\nSorted Numbers "
for (( i=0; i < $n; i++ ))
do
echo ${nos[$i]}
done

---------------------------------------------------------------------------

16 -----------------


  
echo "The Fibonacci series is : "
N=6
a=0
b=1 
for (( i=0; i<N; i++ ))
do
    echo -n "$a "
    fn=$((a + b))
    a=$b
    b=$fn
done
--------------------------------
17-1
for a in 1 2 3 4 5 6 7 8 9 10
do
    # if a = 5 then continue the loop and
    # don't move to line 8
    if [ $a == 5 ]
    then
        continue
    fi
    echo "Iteration no $a"
done
-----------------------------------------------

for f in `find`; do mv -v "$f" "`echo $f | tr '[A-Z]' '[a-z]'`"; done

#!/bin/bash

filesys=(`df | tr -s " " | cut -d " " -f1`)
for j in ${filesys[@]}
do
        echo "$j"
done
useper=(`df | tr -s " " | cut -d " " -f5 | cut -d "%" -f1`)
for i in `seq $((${#useper[@]}-1))`
do
        if [ ${useper[i]} -ge 90 ]
        then
echo "Filesystem ${filesys[i]} have less than 10% free space"
fi
done


-----------------------


for f in * ; do mv -- "$f" "PRE_$f" ; done
