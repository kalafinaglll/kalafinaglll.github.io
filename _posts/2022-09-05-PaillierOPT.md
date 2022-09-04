---
layout: post
classes:
- landing
- dark-theme
title:  "PaillierOPT"
date:   2022-09-04 20:50:21 +0200
author: lukas
categories: jekyll update
---

## Normal Paillier
paper: <https://eprint.iacr.org/2015/864.pdf>
### Parameters
prime numbers p, q  
$$n = p*q $$  
$$λ = lcm(p − 1, q − 1)$$  
g, with $$g \in \mathbb{Z}_{n^{2}}^{*}$$ and the order of g is a multiple of n  

### Public Key
$$n,g$$

### Private Key
$$p,q,λ$$

### Encryption
plaintext m < n  
select a random r < n such that $$r \in \mathbb{Z}_{n}^{*}$$ 
ciphertext $$c=g^{m} r^{n} \bmod n^{2}$$

### Decryption

ciphertext $$c < n^2$$   
plaintext $$m=\frac{\mathrm{L}\left(c^{\lambda} \bmod n^{2}\right)}{\mathrm{L}\left(g^{\lambda} \bmod n^{2}\right)} \bmod n$$  
$$ L(u)=\frac{u-1}{n} $$  


