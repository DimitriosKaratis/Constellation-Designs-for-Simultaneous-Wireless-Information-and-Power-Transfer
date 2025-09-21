# Constellation Designs for Simultaneous Wireless Information and Power Transfer (SWIPT)

This repository contains the project for the course **Telecommunication Systems II**, at the **Department of Electrical and Computer Engineering, Aristotle University of Thessaloniki.**
The goal is to analyze and design constellations for **Simultaneous Wireless Information and Power Transfer (SWIPT)**, focusing on the trade-off between **Peak-to-Average Power Ratio (PAPR)** (linked to energy harvesting) and **Symbol Error Probability (SEP)** (linked to minimum Euclidean distance, dmin).

---

## 📌 Project Tasks

1. **PAPR vs dmin Analysis**
   - Theoretical derivation of PAPR behavior for:
     - 16-PAM
     - 16-PSK
     - 16-QAM
     - 16-Circular QAM (CQAM)
   - Simulation results confirming theoretical findings.

2. **SEP vs Energy Harvesting and SNR**
   - Analysis of Symbol Error Probability (SEP) against:
     - Normalized harvested energy (fixed SNR).
     - SNR (fixed harvested energy).
   - Verification through both theory and simulation.
   - Inclusion of one state-of-the-art SWIPT constellation from literature.

3. **Constellation Design Beyond State-of-the-Art**
   - Proposal of optimized constellations to further balance **error performance** and **energy harvesting efficiency**.

---

## 🛠️ Methodology

- Derived closed-form expressions for **PAPR** and **SEP** for the different constellations.
- Conducted MATLAB/Python simulations to verify theoretical predictions.
- Designed **CQAM constellations with multiple circles** (e.g., N=4, N=8) by calculating optimal radii to maximize performance trade-offs.
- Compared performance to existing schemes from [R1] and [R2].

---

## 📊 Results & Conclusions

- **16-PAM:**  
  - PAPR is **constant** and independent of dmin.  
  - Achieves a PAPR of ≈ **2.6471**.

- **16-PSK:**  
  - PAPR = **1**, independent of dmin, due to equal energy symbols on a circle.  
  - Lowest PAPR but worse SEP compared to QAM.

- **16-QAM:**  
  - Achieves a PAPR of **1.8**, also independent of dmin.  
  - Balances SEP and energy harvesting moderately well.

- **16-CQAM:**  
  - Shows clear **trade-off behavior** between SEP and harvested energy.  
  - By adjusting the number of circles (N=4 vs N=8), different balances can be achieved:
    - More circles → higher harvested energy but higher error probability.
    - Fewer circles → better SEP but reduced energy harvesting.

- **Overall Conclusion:**  
  - Traditional constellations (PAM, PSK, QAM) have fixed PAPR values independent of dmin.  
  - CQAM introduces flexibility, making it more suitable for SWIPT where both **error rate** and **energy efficiency** matter.  
  - Our results confirmed the findings of [R1] and [R2], while also extending them with new constellation designs.

---

## 📚 References

- [R1] G. M. Kraidy, C. Psomas and I. Krikidis, *"Fundamentals of Circular QAM for Wireless Information and Power Transfer,"* IEEE SPAWC, 2021.  
- [R2] M. J. L. Morales, K. Chen-Hu and A. G. Armada, *"Optimum Constellation for Symbol-Error-Rate to PAPR Ratio Minimization in SWIPT,"* IEEE VTC-Spring, 2022.
