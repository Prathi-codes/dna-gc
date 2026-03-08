# dna-gc
Beginner python tool that calculates the GC content of a given DNA sequence
#Program to calculate GC content in a given DNA sequence
import sys
base_code=input("Enter a DNA sequence: ").upper()
g=0
c=0
a=0
t=0
for i in base_code: 
      if i not in "ATGC":
            print("INVALID SEQUENCE")
            sys.exit()
      else:  
           if i=="G":
               g+=1
           elif i=="C":
               c+=1
           elif i=="A":
                a+=1
           else:
                t+=1      
gc_content=((g+c)/(a+g+c+t))*100 
print("The GC content of the given nucleotide code is =", round(gc_content,3),"%")
