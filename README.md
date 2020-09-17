Constructing a Synthetic NMR Well-log using Machine Learning


Executive Summary:

The nuclear magnetic resonance (NMR) log is a useful tool to understand lithological information such as the variation of pore size distribution with depth, but it may not be measured in all wells. The project attempts to predict a missing well log from other available well logs using machine learning tools, more specifically an NMR well log from the measured Gamma Ray (GR) log, Caliper log, Resistivity log, and the interpreted porosity from one well at the Keathley Canyon in the Gulf of Mexico. The constructed model is then used to predict the NMR log at Walker Ridge in Gulf of Mexico, which is another nearby site of methane hydrate accumulation.

In Keathley Canyon Block 151 (KC-151), the analyzed well was drilled and logged during Leg I of the U.S. Department of Energy/Chevron Gas Hydrate Joint Industry Project (JIP) (Ruppel et al., 2008). At Walker Ridge 313 (WR-313), the analyzed well was drilled and logged during JIP Leg II (Collett et al., 2012). The raw well logs for KC-151 are available here and for WR-313 are available here. The processed well logs used in this project for KC-151 are available here and for WR-313 are available here.

Approach:

For an easier characterization of the NMR data, the NMR log, i.e. relaxation time distribution was converted into Mean of T2 (MLT2) and Standard Deviation of T2 (SDT2) which are considered as the two response features to be predicted. The other well logs: GR, Caliper, Resistivity, and the interpreted porosity are the predictor features used to train the model.

An initial analysis is conducted on the well logs to check the univariate and bivariate distributions of the data, and the well-logs are plotted with depth.

Then a linear regression is conducted for both MLT2 and SDT2 using the other predictor variables to observe the behavior with a basic model. It is seen that the linear regression could not capture the response behavior well due to noise, i.e. short-distance variations as well as non-linearities in the data relationships.

This is followed by feature standardization before applying more complex models to reduce effect of outliers and predictor features having different units. Feature ranking was conducted to compare the order in which predictor variables affect the response variables.

Then, the logs are processed to reduce noise, and after a train-test split, polynomial regression modeling is conducted to predict the NMR log at Keathley Canyon until a good fit is obtained.

Finally, the trained model is used to predict the NMR log at Walker Ridge where it was not recorded.