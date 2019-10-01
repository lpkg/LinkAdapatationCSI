# Wireless link adaptation with outdated CSI -- a hybrid data-driven and model-based approach

## Introduction
This GitHub repository complements our paper [[1]](#ourpaper). In this repository, you can find the code to produce all the plots in the paper. We address the issue of **link adaptation** in presence of outdated channel state information (CSI) at the base station. 
There is a time delay between pilot transmission, CSI feedback reception at the base station, and eventual data transmission. During this time, called **feedback delay**, the wireless channel can vary substantially, nullifying the benefits of link adaptation, as the transmission parameters are matched to a channel that is no longer in effect at transmission time.
In order to compensate for this feedback delay, in our paper we propose a **hybrid** approach based on i) an FIR Wiener filter used to predict the instantaneous CSI from some past channel history available at the BS and ii) a neural network, whose input is the Wiener's prediction, used to select the optimal MCS for the data transmission. We also contrast our approach with an **end-to-end** (E2E) approach, based on a neural network which directly takes in input the channel history and selects the optimal CSI. Finally, in our paper, we present a **delay-blind** approach which assumes that the outdated CSI at the BS is actually up-to-date. We use this method as a baseline to show the degrading effects of outdated CSI on the system performance.
In this repository, the reader can investigate and explore the three link adaptation methods mentioned above, i.e., hybrid, E2E, and delay-blind, under two different experimental scenarios:
