# linux-awk-
awk ' NR==FNR{a[$0]=1} NR>FNR&&($1 in a){print}  ' InputFile1 InputFile2
awk ' 
    NR==FNR{a[FNR]=$0}
    NR>FNR&&a[FNR]==$0{print}  
' InputFile1 InputFile2

