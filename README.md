# Maths_python
# Practical 1 – Create and transform vectors and matrices


# import sympy as sp

# # Create a matrix
# A = sp.Matrix([[1, 2], [3, 4]])

# # Create a vector
# B = sp.Matrix([1, 2, 3])

# # Transpose
# print("Transpose:")
# print(A.T)

# # Conjugate transpose
# print("Conjugate Transpose:")
# print(A.conjugate().T)

# # Display vector
# print("Vector:")
# print(B)



# Practical 2 – Echelon form and rank



# import sympy as sp

# A = sp.Matrix([
#     [1, 2, 3],
#     [2, 4, 6],
#     [1, 1, 1]
# ])

# print("Echelon Form:")
# print(A.echelon_form())

# print("Rank:")
# print(A.rank())


# Practical 3 – Cofactors, determinant, adjoint and inverse


# import sympy as sp

# A = sp.Matrix([[1, 2], [3, 4]])

# print("Determinant:", A.det())
# print("Cofactor Matrix:", A.cofactor_matrix())
# print("Adjoint:", A.adjugate())
# print("Inverse:", A.inv())


# Practical 4 – Gauss Elimination Method



# import sympy as sp

# A = sp.Matrix([
#     [1, 1],
#     [1, -1]
# ])

# B = sp.Matrix([5, 1])

# print("Solution:")
# print(A.inv() * B)


# Practical 5 – Gauss-Jordan Method


# import sympy as sp

# A = sp.Matrix([
#     [1, 1, 5],
#     [1, -1, 1]
# ])

# print("Reduced Row Echelon Form:")
# print(A.rref())




# Practical 6 – Basis of column space, null space, row space and left null space


# import sympy as sp

# A = sp.Matrix([
#     [1, 2],
#     [2, 4],
#     [3, 6]
# ])

# print("Column Space:")
# print(A.columnspace())

# print("Row Space:")
# print(A.rowspace())

# print("Null Space:")
# print(A.nullspace())

# print("Left Null Space:")
# print(A.T.nullspace())



# Practical 7 – Linear Dependence, Linear Combination and Transition Matrix



# import sympy as sp

# A = sp.Matrix([
#     [1, 2],
#     [2, 4]
# ])

# print("Rank:", A.rank())
# print("Number of columns:", A.cols)

# if A.rank() == A.cols:
#     print("Linearly Independent")
# else:
#     print("Linearly Dependent")



# Practical 8 – Gram-Schmidt Orthogonalization




# import sympy as sp

# v1 = sp.Matrix([1, 0])
# v2 = sp.Matrix([1, 1])

# u1 = v1
# u2 = v2 - (v2.dot(u1)/u1.dot(u1))*u1

# e1 = u1 / sp.sqrt(u1.dot(u1))
# e2 = u2 / sp.sqrt(u2.dot(u2))

# print("Orthonormal Basis:")
# print(e1)
# print(e2)



# Practical 9 – Eigenvalues, Eigenvectors and Cayley-Hamilton Theorem




# import sympy as sp

# A = sp.Matrix([
#     [2, 0],
#     [0, 3]
# ])

# print("Eigenvalues:")
# print(A.eigenvals())

# print("Eigenvectors:")
# print(A.eigenvects())

# print("Is Diagonalizable?")
# print(A.is_diagonalizable())



# Practical 10 – Coding and Decoding Messages using Matrices



# import sympy as sp

# K = sp.Matrix([
#     [1, 1],
#     [0, 1]
# ])

# P = sp.Matrix([1, 2])

# # Encoding
# C = K * P

# print("Encoded:", C)

# # Decoding
# decoded = K.inv() * C

# print("Decoded:", decoded)


# Practical 11 – Gradient of a Scalar Field



# import sympy as sp

# x, y, z = sp.symbols('x y z')

# f = x**2 + y**2 + z**2

# gradient = [
#     sp.diff(f, x),
#     sp.diff(f, y),
#     sp.diff(f, z)
# ]

# print("Gradient:", gradient)


# Practical 12 – Divergence of a Vector Field



# import sympy as sp

# x, y, z = sp.symbols('x y z')

# P = x
# Q = y
# R = z

# div = sp.diff(P,x) + sp.diff(Q,y) + sp.diff(R,z)

# print("Divergence:", div)



# Practical 13 – Curl of a Vector Field




# import sympy as sp

# x, y, z = sp.symbols('x y z')

# F = sp.Matrix([
#     x*y,
#     y*z,
#     z*x
# ])

# curl = sp.Matrix([
#     sp.diff(F[2],y) - sp.diff(F[1],z),
#     sp.diff(F[0],z) - sp.diff(F[2],x),
#     sp.diff(F[1],x) - sp.diff(F[0],y)
# ])

# print("Curl:")
# print(curl)
