## Homework 1

### 高秋爽 2019212705

#### Problem 1

Fixed Ordering Cost $S = \$1200$

Annual Demand $D = 1800 * 12 = 21600$

Material Cost $C = \$500$

Holding Cost Per Year $hC = 0.2*500 = \$100$

In terms of EOQ model, the optimal lot size is
$$
Q^* = \sqrt{\frac{2DS}{hC}} = \sqrt{\frac{2*21600*1200}{100}} =720
$$
The cycle inventory is $\dfrac{Q^*}{2}=360$

So the firm should load 720 units onto each truck, the cycle inventory of engines at the firm is 360.

#### Problem 3

Fixed Ordering Cost $S = \$250$

Annual Demand $D = 1000$

Holding Cost $H = \$50$

In terms of EOQ model, the optimal lot size is
$$
Q^* = \sqrt{\frac{2DS}{H}} = \sqrt{\frac{2*1000*250}{50}} =100
$$
So Ray should order 100 units each time.

Order Cycle Time $T = \dfrac{Q}{D} = 0.1\  year$ 

- If the order lead time is 1 month, $L = \dfrac{1}{12}\ year < T$ ,$ROQ = \frac{LQ}{T} = \frac{1/12*100}{0.1}\approx 83.3$
- If the order lead time is 4 months, $L = \dfrac{1}{3}\ year > T$ ,$ROQ = \frac{(L\%T)*Q}{T} = \frac{(1/3\%0.1)*100}{0.1}\approx 33.3$

So if lead time is 1 month, he should place the order when the inventory is reduced to 83.3; if lead time is 4 months, he should place the order when the inventory is reduced to 33.3.

#### Problem 5

Components purchased from Supplier A: $D_1 = 20000*12=240000, C_1 =\$5$

Components purchased from Supplier B: $D_2 = 2500*12=30000, C_2 =\$4$

Components purchased from Supplier C: $D_3 = 900*12=10800, C_3 =\$5$

Fixed Ordering Cost $S = \$400$, additional charge $s_1 = s_2 = s_3 = \$100$

Fixed Ordering Cost for each supplier $S_1=S_2=S_3 = \$500$, $h=20\%$

**Current Strategy**

For the current strategy of ordering separately from each supplier , the total cost is 
$$
TC_{current} = \sqrt{2D_1S_1hC_1}+\sqrt{2D_2S_2hC_2}+\sqrt{2D_3S_3hC_3} \approx \$23677.25
$$
Cycle inventory for each component is
$$
\frac{Q_1}{2} = \frac{1}{2}\sqrt{\frac{2D_1S_1}{hC_1}} = 7745.97\\
\frac{Q_2}{2} = \frac{1}{2}\sqrt{\frac{2D_2S_2}{hC_2}} = 3061.86\\
\frac{Q_3}{2} = \frac{1}{2}\sqrt{\frac{2D_3S_3}{hC_3}} = 1643.17
$$
**Strategy 1. Ordered jointly for all three suppliers**
$$
S^* = S + s_1+s_2+s_3 = \$700\\
n^* = \sqrt{\dfrac{h(C_1D_1+C_2D_2+C_3D_3)}{2S^*}}\approx \$14.01\\
TC_1 = n^*S^*+\dfrac{C_1D_1+C_2D_2+C_3D_3}{2n^*}\approx \$19614.28\\
$$
So this strategy will save $\$23677.25-\$19614.28 = \$4062.97$

**Strategy 2. Ordered jointly for a subset of products**

For each product $i$, evaluating the ordering frequency :
$$
	\bar{n}_i = \sqrt{\dfrac{hC_iD_i}{2(S+s_i)}} \qquad \bar{n}_1=15.49,\bar{n}_2=4.90,\bar{n}_3=3.29
$$
So $\bar{n}=\max_i{\bar{n}_i}=\bar{n}_1=15.49$,  $i^* = \arg\max_i{\bar{n}_i}=1$
For all products $i\neq i^*$,evaluating the ordering frequency :
$$
\overset{=}{n}_i=\sqrt{\dfrac{hC_iD_i}{2s_i}}	\qquad \overset{=}{n}_2=10.95,\overset{=}{n}_3=7.35
$$
For all products $i\neq i^*$,evaluate the frequency of product $i$ relative to the most frequently ordered product $i^*$ to be $m^*$:
$$
m_i = \lceil\dfrac{\bar{n}}{\overset{=}{n}_i}\rceil\qquad m_1=1,m_2=2,m_3=3
$$
Recalculate the ordering frequency of the most frequently ordered product $i^*$ to be $n$:
$$
n=\sqrt{\dfrac{\sum_{i=1}^3hC_im_iD_i}{2(S+\sum_{i=1}^3s_i/m_i)}}=16.57
$$
For each product,order frequency $n_i = n/m_i$, so $n_1=16.57,n_2=8.29,n_3=5.52$
$$
TC_2=nS+\sum_{i=1}^3n_is_i+\sum_{i=1}^3\left(\dfrac{D_i}{2n_i}\right)hC_i=\$19333.79
$$
So this strategy will save $\$23677.25-\$19333.79 = \$4343.46$

So I suggest the strategy 2, which is to order jointly for a subset of products.

Order size:
$$
 Q_i'=\dfrac{D_i}{n_i}\qquad Q_1'=14484.01,Q_2'=3618.82,Q_3'=1956.52
$$
Cycle inventory=$\dfrac{1}{2}Q'$ ,$\dfrac{Q_1'}{2} =7242.00,\dfrac{Q_2'}{2} = 1809.41,\dfrac{Q_3'}{2}=978.26$

The cycle inventory of each component under strategy 2 is less than the cycle inventory under current strategy.

#### Problem 7

$D=2000\times12=240000\ units,\ S=\$400,\ h=20\%$
$q_0=0,\ q_1=20000,\ q_2=40000$
$C_0=\$1,\ C_1=\$0.98,\ C_3=\$0.96$
$V_0 = 0,\ V_1 = C_0(q_1-q_0)=\$20000,\ V_2=C_0(q_1-q_0)+C_1(q_2-q_1)=\$39600$
$$Q_i=\sqrt{\frac{2D(S+V_i-C_iq_i)}{hC_i}},\qquad Q_0=30983.87,\ Q_1=44262.67,\ Q_2=63245.55$$
$Q_0 > q_1$, so $Q_0^*=q_1=2000$
$Q_1 > q_2$, so $Q_1^*=q_2=4000$
$Q_2 > q_2$, so $Q_2^*=Q_2=63245.55$
$$TC_i=\dfrac{D}{Q_i}(V_i+C_i (Q_i-q_i))+\dfrac{Q_ih}{2}\dfrac{V_i+C_i(Q_i-q_i )}{Q_i}+\dfrac{D}{Q_i}S$$
So $TC_0=246800,TC_1=243960,TC_2=242663.15$
So optimal lot size is $Q_2^*=63245.55$, cycle inventory is  $\dfrac{Q_2}{2}=31622.78$

#### Problem 9

$D = 300/week\ \ \sigma_D = 200 \ \ L = 2\ weeks\ \ CSL = 0.95$
$\sigma_L = \sqrt{L}\sigma_D \approx 282.84\ \ D_L =LD = 600 $
$ss = F^{-1}_S(CSL)*\sigma_L\approx 465.23$
$ROQ = ss + D_L = 1065.23$
So Best Buy should carry 465.23 safety inventory of cell phones and ROQ is 1065.23.

#### Problem 11

$D = 250/week\ \ \sigma_D = 150 \ \ L = 2\ weeks\ \ Q = 1000\ \ ROP = 600$
$\sigma_L = \sqrt{L}\sigma_D \approx 212.13\ \ D_L =LD = 500 $
$ss = ROP - D_L = 100$
$CSL = F(ROP,D_L,\sigma_L) \approx 0.68$
$ESC = -ss[1-F_s(\dfrac{ss}{\sigma_L})]+\sigma_Lf_s(\dfrac{ss}{\sigma_L}) = -100[1-F_s(\dfrac{100}{212.13})]+212.13f_s(\dfrac{100}{212.13})\approx 43.86$ 
$fr = 1-\dfrac{ESC}{Q} = 0.95614$
So Sams Club store should carry 100 safety inventory, the CSL is 0.68 and fill rate is 0.95614.

#### Problem 13

$k = 900\ \ h = 0.25\ \ L = 4\ weeks\ \ CSL = 0.95$
**(1) size large khaki pants:**
$D = 800/week\ \ \sigma_D = 100\ \ C = 30$
$D^C = kD = 720000\ \ \sigma_D^C = \sqrt{k}\sigma_D = 3000\ \  H = hC =7.5$ 
reduction in holding cost per unit sold:
$$
\dfrac{F^{-1}_S(CSL)\times\sqrt{L}\times H}{D^C} \times (k\sigma_D - \sigma_D^C)\approx 2.98
$$
**(2) purple cashmere sweaters:**
$D = 50/week\ \ \sigma_D = 50\ \ C = 100$
$D^C = kD = 45000\ \ \sigma_D^C = \sqrt{k}\sigma_D = 1500\ \  H = hC =25$ 
reduction in holding cost per unit sold:
$$
\dfrac{F^{-1}_S(CSL)\times\sqrt{L}\times H}{D^C} \times (k\sigma_D - \sigma_D^C)\approx 79.50
$$
Gap should carry pants at stores and carry sweaters at the central warehouse for the online channel, because reduction in holding cost per unit sold on moving sweaters from the stores to the online channel is much higher than that on moving pants.