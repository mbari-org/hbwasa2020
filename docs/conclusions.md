# Summary and Conclusions

- Based on classification performance,
  we empirically determined some potentially good values for signal processing parameters:
  LPC order: 80–120; Window analysis size: 45–120ms; Window offset: 15ms.

- The resulting levels of classification accuracy, ranging between 88% and 94%, are encouraging.

- The relative accuracy of different methods was consistent regardless of parameterization.

- The VQ classifier allowed us to validate the LPC analysis and clustering phases of our pipeline,
  while providing a baseline for comparison with the probabilistic models.

- The Naive Bayes classifier showed great performance despite its simplicity and strong underlying assumption.

- Although being the least performant, the Markov Chain classifier allowed us to
  incorporate time dependency as well as a baseline to compare results against
  other methods, in particular the HMM.

- The HMM model consistently provided the best performance among the probabilistic models, 
  though just slightly better than Naive Bayes. This is likely due to overfitting,
  especially given the small size of the dataset, as well as the limited power of
  using discrete observation distributions [7].

## Conclusion and Future Work

The scale of the work described here is admittedly limited in terms of the labelling
itself still being preliminary and the analysis done on segments extracted from a small,
continuous 4.5 hour recording.
With the results being obtained, however, we see potential in extending and
refining the methods. Our future efforts include:

- Larger scale model training and tuning
- Gaining more insights toward a definition of building blocks for charaterization of
   humpback whale song structure
- Inclusion of additional features from the signal analysis
  (e.g., cepstral related coefficients), 
  and use of HMM with continuous observation densities (e.g., Gaussian Mixture Models)
- Automated segmentation toward an operational use of the classification techiques


## Acknowledgments

The NSF funded installation and maintenance of the MARS cabled observatory
through awards 0739828 and 1114794. Hydrophone recording through MARS was
supported by the Monterey Bay Aquarium Research Institute, through a
grant from the David and Lucile Packard Foundation.
