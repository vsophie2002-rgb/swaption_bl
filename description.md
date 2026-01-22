# swaption_bl
This project applies the logic of Breeden-Litzenberger to extract conditional densities from swaption prices around important FOMC decisions. The data was extracted from Bloomberg, and contains the normal implied volatilites of +-200bps ATM for 3 month - 1 year payer swaption contracts. "Call" prices were computed using the Bachelier formula, with setting F=0. The results therefore should be interpreted relative to the forward swap rate. 
Due to the sparse nature of the strike grid, instead of taking the second derivative of the call price w.r.t K, a discrete differentiation method was applied, computing the change of slope relative to the change in strikes between two points of the grid. This yields atomic densities at each strike point, from which the conditional moments were calculated directly. Kernel smoothing is only used for visualisation purposes, with the base of the kernel = 25bps. 


