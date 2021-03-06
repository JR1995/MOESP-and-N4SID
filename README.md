# MIMO linear system identification

MIMO linear system identification using commom subspace methods is an active area, many algorithms were develop in recent years. I implemented well known methods called MOESP and N4SID during my master degree.

## MOESP

 MOESP (Multivariable Output-Error State sPace) is a deterministic method to identify linear time invariant systems. The MOESP method developed by M. Verhaegen and P. Dewilde is based on the **LQ decomposition** of Hankel matrix formed from input-output data, where L is lower triangular and Q is orthogonal. A **Singular Value Decomposition (SVD)** can be performed on a block from the L (L22) matrix to obtain the system order and the extended observability matrix. From this matrix it is possible to estimate the matrices C and A of state-space model. The final step is to solve overdetermined linear equations using the least-squares method to calculate matrices B and D.


 <p align="center">
 <img src="https://github.com/Alro10/MOESP-and-N4SID/blob/master/moesp_output.jpg" alt="alt text" width="80%" height="80%">
 </p>

 ## N4SID:

 N4SID (Numerical Algorithms for Subspace State Space System Identification) developed by P. Van Overschee and B. De Moor. The method stars with the oblique projection of the future outputs to past inputs and outputs into the future inputs direction. The second step is to apply the **LQ decomposition** and then the state vector can be computed by the **SVD**. Finally, it is possible to compute the matrices A, B, C and D of state-space model by using the least-squares method.

 <p align="center">
 <img src="https://github.com/Alro10/MOESP-and-N4SID/blob/master/n4sid_output.jpg" alt="alt text" width="80%" height="80%">
 </p>

## Testing
This is the available benchmark:

```python
 x(t+1) = A*x(t) + B*u(t)
 y(t)   = C*x(t) + D*u(t)
 ```

If you have questions or problems, please open an issue or, even better, fix the problem yourself and submit a pull request!

## Citing

If you use `MOESP-and-N4SID` in your research, you can cite it as follows:
```bibtex
@misc{robles2017subspace,
    author = {Alexander Robles},
    title = {MOESP-and-N4SID},
    year = {2017},
    publisher = {GitHub},
    journal = {GitHub repository},
    howpublished = {\url{https://github.com/Alro10/MOESP-and-N4SID}},
}
```
