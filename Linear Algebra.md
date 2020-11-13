#### Vector
$$
\mathbf{x} = \left [ \begin{matrix}
x_1 \\\\
x_2 \\\\
\vdots \\\\
x_n
\end{matrix} \right ]
$$

#### Scalar product

$$
\mathbf{w} \cdot \mathbf{x} = \sum_{i=1}^{n}w_i x_i
$$

#### Angle between vectors in n dimensional space

$$
\mathbf{w} \cdot \mathbf{x} = |\mathbf{w}| |\mathbf{x}| \cos(\theta)
$$

Scalar product as projection: projection of vector $\mathbf{x}$ on a direction specified by vector $\mathbf{u}$ 
$$
\frac{\mathbf{x} \cdot \mathbf{u}}{\left | \mathbf{u} \right |^{2}} \mathbf{u}
$$

another format

$$
\frac{\mathbf{x}^{T} \mathbf{u}}{\left | \mathbf{u} \right |^{2}} \mathbf{u}
$$

#### Matrix

$$
\mathbf{A} = \left [ \begin{matrix}
a_{11} & a_{12} & \cdots & a_{1d}\\\\
a_{21} & a_{22} & \cdots & a_{2d}\\\\
\vdots & \vdots & \vdots & \vdots\\\\
a_{n1} & a_{n2} & \cdots & a_{nd}
\end{matrix} \right ]
$$

#### Identity matrix

$$
\mathbf{I} = \left [ \begin{matrix}
1 & 0 & \cdots & 0\\\\
0 & 1 & \cdots & 0\\\\
\vdots & \vdots & \vdots & \vdots\\\\
0 & 0 & \cdots & 1
\end{matrix} \right ]
$$

#### Square matrix

$$
\mathbf{A} = \left [ \begin{matrix}
a_{11} & a_{12} & \cdots & a_{1n}\\\\
a_{21} & a_{22} & \cdots & a_{2n}\\\\
\vdots & \vdots & \vdots & \vdots\\\\
a_{n1} & a_{n2} & \cdots & a_{nn}
\end{matrix} \right ]
$$

##### Operations

Add

$A=(a_{ij}): p \times q$,$B=(b_{ij}): p \times q$

$$
A + B = (a_{ij} + b_{ij}): p \times q
$$
Multiplication

$c$ is constant
$$
cA=(ca_{ij}): p \times q
$$
$A=(a_{ij}): p \times q$,$B=(b_{ij}): q \times r$

$$
AB = \left( \sum_{k=1}^q a_{ik} b_{kj} \right ): p \times r
$$

Properties of Matrix Multiplication

$$
A(B_1 B_2) = (A B_1) B_2 
\\\\
A(B_1 + B_2) = AB_1 + AB_2
\\\\
(B_1 + B_2)A = B_1A + B_2A
\\\\
c(A + B) = cA + cB
\\\\
c(AB) = (cA)B = A(cB)
\\\\
I_mA = A = AI_n
$$

Transpose

$$
\mathbf{A^T} = \mathbf{{A}'} = \left [ \begin{matrix}
a_{11} & a_{21} & \cdots & a_{n1}\\\\
a_{12} & a_{22} & \cdots & a_{n2}\\\\
\vdots & \vdots & \vdots & \vdots\\\\
a_{1d} & a_{2d} & \cdots & a_{nd}
\end{matrix} \right ]
$$

Properties of identity matrix

$$
(A^T)^T = A
\\\\
(A + B)^T = A^T + B^T
\\\\
(cA)^T = cA^T
\\\\
(AB)^T = B^T A^T
$$

Property of symmetric matrix

$$
A^T = A
$$

Determinant of a square matrix

$$
det\left [ \begin{matrix}
a & b\\\\
c & d
\end{matrix} \right ] = ad - bc
$$

$A=(a_{ij}): n \times n$

$$
det(A) = \sum_{j=1}^{n} (-1)^{1+j}a_{1j}det(A_{1j})
$$
example:

$$
A = \left [ \begin{matrix}
1 & 5 & 0\\\\
2 & 4 & -1\\\\
0 & -2 & 0
\end{matrix} \right ]

det(A) = a_{11}det(A_{11}) - a_{12}det(A_{12}) + a_{13}det(A_{13}) 
\\\\
= 1 \times det \left [ \begin{matrix}
4 & -1\\\\
-2 & 0
\end{matrix} \right ] - 5 \times det \left [ \begin{matrix}
2 & -1\\\\
0 & 0
\end{matrix} \right ] + 0 \times det \left [ \begin{matrix}
2 & 4\\\\
0 & -2
\end{matrix} \right ]
$$


Inverse matrix

$$
A = \left [ \begin{matrix}
a & b\\\\
c & d
\end{matrix} \right ] \rightarrow 
A^{-1}= \frac{1}{ad-bc}\left [ \begin{matrix}
d & -b\\\\
-c & a
\end{matrix} \right ]
$$

Properties of inverse matrix


$$
(A^{-1})^{-1} = A
\\\\
(AB)^{-1} = B^{-1} A^{-1}
\\\\
(A^T)^{-1} = (A^{-1})^T
$$

Orthogonal matrices

If a square matrix $A$ is orthogonal, if and only if

$$
A^T A = I
$$

Properties of the orthogonal matrix

$$
A^{-1} = A^T
\\\\
A^{-T} = A
\\\\
A^T A = I
\\\\
A A^T = I
\\\\
det(A) = \pm 1
$$

Trace

$$
trace(A) = \sum_{i=1}^n a_{ii}
$$
Properties of trace

$$
trace(A) = \sum_{i=1}^n \lambda_i \qquad \lambda_i = eig(A)
\\\\
trace(A) = trace(A^T)
\\\\
trace(AB) = trace(BA)
\\\\
trace(A+B) = trace(A) + trace(B)
\\\\
trace(ABC) = trace(BCA) = trace(CAB)
\\\\
a^Ta = trace(aa^T)
$$

#### Eigenvalues and Eigenvectors

Eigenvectors $\mathbf{v}_i$ and eigenvalues $\lambda_i$

$$
\mathbf{A} \mathbf{v}_i = \lambda_i \mathbf{v}_i
$$

Properties

$\mathbf{A}: n \times m, \qquad \mathbf{B}: m \times n$
$$
\mathrm{eig}(\mathbf{A} \mathbf{B}) = \mathrm{eig}(\mathbf{B} \mathbf{A})
$$

$\mathbf{A}$ is symmetric, then
$$
\mathbf{V} \mathbf{V}^T = \mathbf{I} \qquad (\mathrm{i.e.} \; \mathbf{V} \; \mathrm{is} \; \mathrm{orthogonal})
\\\\
\lambda_i \in \mathbb{R} \qquad (\mathrm{i.e.} \; \lambda_i \; \mathrm{is} \; \mathrm{real})
\\\\
trace(\mathbf{A}^p) = \sum_i \lambda_i^p
\\\\
eig(\mathbf{I} + c \mathbf{A}) = 1 + c \lambda_i
\\\\
eig(\mathbf{A} - c \mathbf{I}) = \lambda_i - c
\\\\
eig(\mathbf{A}^{-1}) = \lambda_i^{-1}
$$

Positive definite matrix
$$
x^T \mathbf{A} x > 0, \forall x \neq 0 \rightarrow \mathbf{A} \; \mathrm{is} \; \mathrm{positive} \; \mathrm{definite} \; \mathrm{matrix}
$$
Properties

If $\mathbf{A}$ is positive definite, then $\mathbf{A}$ is invertible and $\mathbf{A}^{-1}$ is also positive definite

If $\mathbf{A}$ is positive definite, then $A_{ii}>0, \forall i$

The matrix $\mathbf{A}$ is positive definite $\Leftrightarrow$ there exits an invertible matrix $\mathbf{B}$ such that $\mathbf{A} = \mathbf{B} \mathbf{B}^T$

For a symmetric, positive matrix $\mathbf{A}$
$$
\mathrm{eig}(\mathbf{A}^T \mathbf{A}) = \mathrm{eig}(\mathbf{A} \mathbf{A}^T)
$$

#### Singular Value Decomposition

$\mathbf{A}: n \times m$

$$
\mathbf{A} = \mathbf{U} \mathbf{D} \mathbf{V}^T
\\\\
\mathbf{U} = \mathrm{eigenvectors} \; \mathrm{of} \; \mathbf{A} \mathbf{A}^T \qquad n \times n
\\\\
\mathbf{D} = \sqrt{diag(\mathrm{eig}(\mathbf{A} \mathbf{A}^T))} \qquad n \times m
\\\\
\mathbf{V} = \mathrm{eigenvectors} \; \mathrm{of} \; \mathbf{A}^T \mathbf{A} \qquad m \times m
$$
