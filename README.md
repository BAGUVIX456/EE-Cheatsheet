# Engineering Economy Cheatsheet

- **<u>Terminology</u>:**
	- i : Interest rate in %
	- N : no. of compounding periods/interest period
	- P : Present value of money
	- F : Future worth of money
	- A : End of period cashflow or annuity
	- G : Arithmetic gradient (amount by which cash flow is increased at the end of every period)
	- MARR : Minimum Attractive Rate of Return

<br />

- **<u>Future worth of a single present value:</u>**
	$$F = P*(1+i)^N=P\left( \frac{F}{P},\ i\%,\ N \right)$$ 
	- $(i+i)^N$ is called <mark style="background: #FF5582A6;">Single Payment Compound Amount Factor</mark>
	- $(1+i)^{-N}$ is called <mark style="background: #FF5582A6;">Single Payment Present Worth Factor</mark>

<br />


- **<u>Present value of uniform annuity</u>:**
	$$P=A\left( \frac{(1+i)^N-1}{i*(1+i)^N} \right)=A\left( \frac{P}{A},\ i\%, \ N \right)$$
	- $\left( \frac{(1+i)^N-1}{i*(1+i)^N} \right)$ is called <mark style="background: #FF5582A6;">Series Present Worth Factor</mark>
	- The reciprocal of the above is called <mark style="background: #FF5582A6;">Capital Recovery Factor</mark>

<br />


- **<u>Future worth of annuity</u>:**
	$$F=A\left( \frac{(1+i)^N-1}{i} \right)=A\left( \frac{F}{A},\ i\%,\ N\right)$$
	- $\left( \frac{(1+i)^N-1}{i} \right)$ is known as <mark style="background: #FF5582A6;">Uniform Series Compound Amount Factor</mark>
	- The reciprocal of the above is known as <mark style="background: #FF5582A6;">Sinking Fund Factor</mark>

<br />

- **<u>Deffered annuities</u>:**
	If the annuity is deferred for $J$ periods $(J < N)$, the present equivalent at time zero will be $$P_{0}=A\left( \frac{P}{A},\ i\%,\ N-J \right)\left( \frac{P}{F},\ i\%,\ J \right)$$

<br />


- **<u>Present value of G</u>:**
	$$P=G\underbrace{\left( \frac{1}{i} \right)\left[ \frac{(1+i)^N-1}{i*(1+i)^N}\ -  \frac{N}{(1+i)^N}\right]}_{Gradient\ To\ Present\ Worth\ Conversion\ Factor} = G\left( \frac{P}{G},\ i\%,\ N \right)$$

<br />


- **<u>Annual worth of G</u>:**
	$$A=G*\underbrace{\left[ \frac{1}{i}\ - \frac{N}{(1+i)^N-1} \right]}_{\text{Gradient to uniform series conversion factor}} =\  G\left( \frac{A}{G},\ i\%,\ N \right)$$

<br />


- **<u>Present value of geometric gradient series</u>:**
	$$P_{g}=A_{1}\left[ \frac{ 1-\left( \frac{1+g}{1+i} \right)^N}{i-g}\right]=A_{1}\left( \frac{P}{A},\ g\%,\ i\%,\ N \right),\ g\neq i$$
	where:
		$A_1 = \text{initial annual amount}$
		$g = \text{geometric growth rate of gradient series}$

	- For $i=g$
		$$P_{g}=A_{1}\left( \frac{N}{1+i} \right)$$

<br />

- **<u>Present value with varying interest rate given G at end of Nth period</u>:**
	$$P=\frac{F_{N}}{\prod_{k=1}^N (1+i)^k}$$

### Methods for making economic studies

- **Present worth method (PWM):**
	- To determine a project's economic worthiness, we simply compute the present equivalent of all cash flows using the MARR as the interest rate
	- If the present worth is greater than or equal to zero, the project is acceptable
	- $$PW(i\%)=\sum_{k=0}^NF_{k}(1+i)^{-k}$$
<br />


- **Future worth method (FWM):**
	- The FW is based on the equivalent worth of all cash inflows and outflows at the end of the planning horizon (study period) at an interest rate that is generally the MARR
	- If $FW(i=MARR)\geq0$, the project is economically justified
	- $$FW(i\%)=\sum_{k=0}^NF_{k}(1+i)^{N-k}$$

<br />

- **Annual worth method (AWM):**
	- $$AW(i\%)=R-E-CR(i\%)$$
	where, $R=\text{annual equivalent revenues}$
	$E=\text{annual equivalent capital}$
	$CR=\text{annual equivalent capital recovery}$
	<br>
	- $$CR(i\%)=I\left( \frac{A}{P},\ i\%,\ N \right)-S\left( \frac{A}{F},\ i\%,\ N \right)$$
	where, $I=\text{initial investment for the project}$
	$S=\text{salvage value at the end of the study period}$
	$N=\text{project study period}$
	<br>
	- If $AW\geq0$, the project is economically justified
<br>
- **Net present value (NPV) with time:**
	- NPV with annual outflow (A) varying
		$$=\sum_{t=1}^N\frac{C_{t}}{(1+r)^t}-IV$$
		where, $C_{t}=\text{cash flow at the end of year t}$
		$r=\text{rate of discount}$
		$IV=\text{initial investment}$
	<br>
	- NPV with time-varying discounts
		$$=\sum_{t=1}^N\frac{C_{t}}{\prod_{j=1}^t(1+r_{j})}-IV$$
<br>
- **Benefit Cost Ratio:**
	- $BCR=\frac{PVB}{I}$ where $PVB=\text{present value of all benefits,}\ I=\text{initial investment}$
	- Net BCR (NBCR) $=\frac{PVB-I}{I}=BCR-1$
	- $BCR>1,\ \text{accept}$
		$BCR<1,\ \text{reject}$
		$BCR=1,\ \text{indifferent}$
<br>
- **Internal Rate of Return Method (IRR):**
	- IRR is the $i'\%$ at which $$\sum_{k=0}^NR_{k}\left( \frac{P}{F},\ i'\%,\ k \right)=\sum_{k=0}^NE_{k}\left( \frac{P}{F},\ i'\%,\ k \right)$$
	where, $R_{k}=\text{net revenues or savings for the kth year}$
	$E_{k}=\text{net expenditures}$
	- In other words, IRR is the discount rate at which NPV is 0
	- If $IRR\geq MARR$, project is economically feasible'
<br>
- **Modified IRR (MIRR):**
	The procedure to find MIRR is
	- $PVC=\sum_{t=0}^N\frac{\text{Cash outflow}_{t}}{(1+r)^t}$
	- Calculate terminal value (TV) of cash inflows
	$TV=\sum_{t=0}^N\text{Cash inflow}_{t}(1+r)^{N-t}$
	- Obtain MIRR using
	$PVC=\frac{TV}{(1+MIRR)^N}$
