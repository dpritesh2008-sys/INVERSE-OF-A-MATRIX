~~~
Name: Ritesh DP
Register No: 212225040339
~~~
# INVERSE-OF-A-MATRIX
## Aim:
To write a python program to find the inverse of a matrix
## Equipment’s required:
1. 	Hardware – PCs
2. 	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:

### Step1 :
Import the numpy module to use the built-in functions for calculation

### Step 2:
Prepare the lists from each linear equations and assign in np.array()

### Step 3:
Using np.linalg.inv(),we can find the inverse of a matrix

### Step 4:
End the program

## Program:
~~~
# Given matrix
A = [[2, 1, 1],
     [1, 1, 1],
     [1, -1, 2]]

# Determinant
det = (A[0][0]*(A[1][1]*A[2][2] - A[1][2]*A[2][1])
      -A[0][1]*(A[1][0]*A[2][2] - A[1][2]*A[2][0])
      +A[0][2]*(A[1][0]*A[2][1] - A[1][1]*A[2][0]))

# Cofactor matrix
cof = [
    [(A[1][1]*A[2][2] - A[1][2]*A[2][1]),
     -(A[1][0]*A[2][2] - A[1][2]*A[2][0]),
     (A[1][0]*A[2][1] - A[1][1]*A[2][0])],

    [-(A[0][1]*A[2][2] - A[0][2]*A[2][1]),
     (A[0][0]*A[2][2] - A[0][2]*A[2][0]),
     -(A[0][0]*A[2][1] - A[0][1]*A[2][0])],

    [(A[0][1]*A[1][2] - A[0][2]*A[1][1]),
     -(A[0][0]*A[1][2] - A[0][2]*A[1][0]),
     (A[0][0]*A[1][1] - A[0][1]*A[1][0])]
]

# Transpose (Adjoint)
adj = [[cof[j][i] for j in range(3)] for i in range(3)]

# Inverse
inv = [[adj[i][j]/det for j in range(3)] for i in range(3)]

# Format like NumPy output
def fmt(x):
    if abs(x - int(x)) < 1e-9:
        return f"{int(x)}."
    else:
        return f"{x:.8f}".rstrip('0')

print(f"[[ {fmt(inv[0][0]):<10} {fmt(inv[0][1]):<10}   {fmt(inv[0][2]):<10}]")
print(f" [{fmt(inv[1][0]):<10}  { fmt(inv[1][1]):<10} {fmt(inv[1][2]):<10}]")
print(f" [{fmt(inv[2][0]):<10}  { fmt(inv[2][1]):<10}  {fmt(inv[2][2]):<10}]]")
~~~
## Output:
<img width="1292" height="342" alt="image" src="https://github.com/user-attachments/assets/40239df4-6cbe-44ef-90ee-c7b46bbae066" />

## Result:
Thus the inverse of given matrix is successfully solved using python program

