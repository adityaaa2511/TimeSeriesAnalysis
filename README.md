# TimeSeriesAnalysis
*This repository contains various statistical, machine learning, deep learning,industrial and unorthodox techniques which I have implemented while learning about Time Series Analysis.*  
PS: I also read a research paper(added to the repo for reference) detailing methods to convert a time series into an image namely:-<br/>1) **Gramian Angular Fields** <br/>2) **Markov Transition Fields** and then train 2-D convolutions instead.~~Maybe I'll write the code for this the next time I feel like messing with time series!!~~ <br/>
So, finally I got the time to explore GAFs and MTFs and I have used these techniques on the LoadGunpoint classification dataset. I have borrowed the CNN structure(I have no idea about Tiled CNNs thus, I decided to use a simpler one) from another research paper (also added to the repo) and achieved a Max Accuracy of **98.67%** using Gramian Angular Summation Fields and a Max Accuracy of **90%** using the Markov Transition Fields.<br/><br/>
*Some insights into GAFs AND MTFs*<br/>
## Gramian Angular Fields
* The Gram matrix is a matrix whose elements are the inner product/dot product between the vectors specified by the indices. Hence, each element is a measure of similarity between the vectors and this is why we use the Gram matrix, as it preserves the **Temporal Relation** between the values at different time intervals.<br/> 
* Now, in order to convert the time series values into vectors we convert them into polar coordinates(as opposed to cartesian coordinates, polar coordinates preserve absolute temporal relations). Another advantage is that the relations are bijective as cos is monotonic is b/w 0 and pie. Thus, given a time series, the proposed conversions produce one and only one result in the polar coordinate system with a unique inverse function.<br/>
* The inner product for the GAF is now defined as Cos(phi1 + phi2) for summation fields and Cos(phi1-phi2) for difference fields.<br/>
## Markov Transition Fields
