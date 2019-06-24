# Construction-of-square-perfect-binary-arrays

Steps to use the perfect binary array in FALP[1]:

1) N=32; % In FALP, we considered a 32x32 UPA, i.e.,  N=32.
2) Matrix=dlmread('PBA_32x32.txt');   % Loads the binary perfect array used in FALP
3) P= Matrix/N;  % P is the base matrix- has unit norm after scaling

%% Some interesting properties of P

A. abs(fft2(P)) is unimodular !! Check out surf(abs(fft2(P)))

B. Any 2D-circulant shift of P is orthogonal to P, i.e., <P,shifted P> =0 !

Note: It can take forever to find a matrix that satisfies any of the above properties using a computer search over {+1,-1}^1024. Perfect binary arrays are very rare in the exponentially large set of binary matrices [2].  


%% Channel measurements can be acquired by applying random 2D-circulant shifts of P to the phased array
%% Recursive construction and partial 2D-DFT-based CS to be posted after publication in IEEE Xplore.


[1] N. J. Myers, A. Mezghani, and R. W. Heath Jr., "FALP: Fast beam alignment in mmWave systems with low-resolution phase shifters" submitted to IEEE Trans. on Communications 2019
[2] J. Jedwab, C. Mitchell, F. Piper, and P. Wild., "Perfect binary arrays and difference sets." Discrete Mathematics 1994
