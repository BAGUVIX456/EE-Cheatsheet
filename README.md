#Engineering Economy Cheatsheet

- **<u>Terminology</u>:**
	- i : Interest rate in %
	- N : no. of compounding periods/interest period
	- P : Present value of money
	- F : Future worth of money
	- A : End of period cashflow or annuity
	- G : Arithmetic gradient (amount by which cash flow is increased at the end of every period)

- **<u>Future worth of a single present value:</u>**
	$$F = P*(1+i)^N$$ 
	- $(i+i)^N$ is called <mark style="background: #FF5582A6;">Single Payment Compound Amount Factor</mark>
	- $(1+i)^{-N}$ is called <mark style="background: #FF5582A6;">Single Payment Present Worth Factor</mark>

- **<u>Present value of uniform annuity</u>:**
	$$P=A\left( \frac{(1+i)^N-1}{i*(1+i)^N} \right)=A\left( \frac{P}{A},\ i\%, \ N \right)$$
	- $\left( \frac{(1+i)^N-1}{i*(1+i)^N} \right)$ is called <mark style="background: #FF5582A6;">Series Present Worth Factor</mark>
	- The reciprocal of the above is called <mark style="background: #FF5582A6;">Capital Recovery Factor</mark>

- **<u>Future worth of annuity</u>:**
	$$F=A\left( \frac{(1+i)^N-1}{i} \right)=A\left( \frac{F}{A},\ i\%,\ N\right)$$
	- $\left( \frac{(1+i)^N-1}{i} \right)$ is known as <mark style="background: #FF5582A6;">Uniform Series Compound Amount Factor</mark>
	- The reciprocal of the above is known as <mark style="background: #FF5582A6;">Sinking Fund Factor</mark>

- **<u>Present value of G</u>:**
	$$P=G\underbrace{\left( \frac{1}{i} \right)\left[ \frac{(1+i)^N-1}{i*(1+i)^N}\ -  \frac{N}{(1+i)^N}\right]}_{Gradient\ To\ Present\ Worth\ Conversion\ Factor} = G\left( \frac{P}{G},\ i\%,\ N \right)$$

- **<u>Annual worth of G</u>:**
	$$A=G*\underbrace{\left[ \frac{1}{i}\ - \frac{N}{(1+i)^N-1} \right]}_{\text{Gradient to uniform series conversion factor}} =\  G\left( \frac{A}{G},\ i\%,\ N \right)$$

- **<u>Present value of geometric gradient series</u>:**
	$$P_{g}=A_{1}\left[ \frac{ 1-\left( \frac{1+g}{1+i} \right)^N}{i-g}\right]=A_{1}\left( \frac{P}{A},\ g\%,\ i\%,\ N \right),\ g\neq i$$
	where:
		$A_1 = \text{initial annual amount}$
		$g = \text{geometric growth rate of gradient series}$

	- For $i=g$
		$$P_{g}=A_{1}\left( \frac{N}{1+i} \right)$$

- 
