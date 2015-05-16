ReadMe file for the NOISE toolbox version 0.12 Monday, July 12, 2004 at 19:07:12
Written by Neil D. Lawrence.

License Info
------------

This software is free for academic use. Please contact Neil Lawrence if you are interested in using the software for commercial purposes.

This software must not be distributed or modified without prior permission of the author.


This toolbox implements different noise models for the IVM toolbox from version 0.31.

Interaction with the toolbox is done through the interface files which are prefixed by `noise'. 

The toolbox was spun out of the IVM toolbox, and most of the files are based on files in IVM 0.221.

Noise Types
-----------

Three main noise models are also provided:

      'gaussian' is the standard Gaussian noise model.

      'probit' is the probit model for classification.

      'ordered' is an ordered categorical model based on the probit.

Also there is

      'cmpnd' is for associating different noise models to different processes when learning multiple processes together. The ability to learn multiple processes is mainly included so that the next release of GPLVM code can use this IVM code base, but it may also be useful for multi-class classification noise models.

      'mgaussian' which is designed to allow multiple processes to have individually different variances (mainly for the GPLVM).

The perl script for generating code for new noise models is noiseGenerator.pl

It is run with two arguments, the first is the short name for the noise model, e.g. gaussian, the second is the long name, e.g. Gaussian\ noise\ model.

File Listing
------------

cmpndLikelihood.m: Likelihood of data under compound noise model.
cmpndLogLikelihood.m: Log-likelihood of data under compound noise model.
cmpndNoiseDisplay.m: Display the parameters of the compound noise model.
cmpndNoiseExpandParam.m: Expand probit noise structure from param vector.
cmpndNoiseExtractParam.m: Extract parameters from compound noise model.
cmpndNoiseGradVals.m: Gradient wrt x of log-likelihood for compound noise model.
cmpndNoiseGradientParam.m: Gradient of the compound noise model's parameters.
cmpndNoiseNuG.m:  Update nu and g parameters associated with compound noise model.
cmpndNoiseOut.m: Output from compound noise model.
cmpndNoiseParamInit.m: Compound noise model's parameter initialisation.
cmpndNoiseSites.m: Site updates for compound noise model.
gaussianLikelihood.m: Likelihood of data under Gaussian noise model.
gaussianLogLikelihood.m: Log-likelihood of data under Gaussian noise model.
gaussianNoise3dPlot.m: Draw a 3D or contour plot for the Gassian noise model.
gaussianNoiseDisplay.m: Display the parameters of the Gaussian noise model.
gaussianNoiseExpandParam.m: Expand Gaussian noise structure from param vector.
gaussianNoiseExtractParam.m: Extract parameters from Gaussian noise model.
gaussianNoiseGradVals.m: Gradient wrt mu and varsigma of log-likelihood for gaussian noise model.
gaussianNoiseGradientParam.m: Gradient of the Gaussian noise model's parameters.
gaussianNoiseNuG.m: Update nu and g parameters associated with Gaussian noise model.
gaussianNoiseOut.m: Output from Gaussian noise model.
gaussianNoiseParamInit.m: Gaussian noise model's parameter initialisation.
gaussianNoisePointPlot.m: Plot the data-points for ordered categorical noise model.
gaussianNoiseSites.m: Site updates for Gaussian noise model.
mgaussianLikelihood.m: Likelihood of data under Variable variance Gaussian noise model.
mgaussianLogLikelihood.m: Log-likelihood of data under Variable variance Gaussian noise model.
mgaussianNoiseDisplay.m: Display  parameters from Variable variance Gaussian noise model.
mgaussianNoiseExpandParam.m: Expand Variable variance Gaussian noise model's structure from param vector.
mgaussianNoiseExtractParam.m: Extract parameters from Variable variance Gaussian noise model.
mgaussianNoiseGradVals.m: Gradient wrt mu and varsigma of log-likelihood for Variable variance Gaussian noise model.
mgaussianNoiseGradientParam.m: Gradient of the Variable variance Gaussian noise model's parameters.
mgaussianNoiseOut.m: Ouput from Variable variance Gaussian noise model.
mgaussianNoiseParamInit.m: Variable variance Gaussian noise model's parameter initialisation.
negNoiseGradientParam.m: Wrapper function for calling noise gradients.
negNoiseLogLikelihood.m: Wrapper function for calling noise likelihoods.
ngaussLikelihood.m: Likelihood of data under noiseless Gaussian noise model.
ngaussLogLikelihood.m: Log-likelihood of data under noiseless Gaussian noise model.
ngaussNoiseDisplay.m: Display  parameters from noiseless Gaussian noise model.
ngaussNoiseExpandParam.m: Expand noiseless Gaussian noise model's structure from param vector.
ngaussNoiseExtractParam.m: Extract parameters from noiseless Gaussian noise model.
ngaussNoiseGradVals.m: Gradient wrt mu and varsigma of log-likelihood for noiseless Gaussian noise model.
ngaussNoiseGradientParam.m: Gradient of the noiseless Gaussian noise model's parameters.
ngaussNoiseNuG.m: Update nu and g parameters associated with noiseless Gaussian noise model.
ngaussNoiseOut.m: Ouput from noiseless Gaussian noise model.
ngaussNoiseParamInit.m: noiseless Gaussian noise model's parameter initialisation.
ngaussNoiseSites.m: Site updates for noiseless Gaussian noise model.
noise3dPlot.m: Draw a 3D or contour plot for the relevant noise model.
noiseCreate.m: Initialise a noise structure.
noiseDisplay.m: Display the parameters of the noise model.
noiseExpandParam.m: Expand the noise model's parameters from params vector.
noiseExtractParam.m: Extract the noise model's parameters.
noiseGradVals.m: Gradient of noise model wrt mu and varsigma.
noiseGradX.m: Returns the gradient of the log-likelihood wrt x.
noiseGradientParam.m: Gradient of the noise model's parameters.
noiseLikelihood.m: Return the likelihood for each point under the noise model.
noiseLogLikelihood.m: Return the log-likelihood under the noise model.
noiseOut.m: Give the output of the noise model given the mean and variance.
noiseParamInit.m: Noise model's parameter initialisation.
noisePointPlot.m: 
noiseTest.m: Run some tests on the specified noise model.
noiseUpdateNuG.m: Update nu and g for a given noise model.
noiseUpdateSites.m: Update site parameters for a given noise model.
orderedGradX.m: Gradient wrt x of log-likelihood for Ordered categorical model.
orderedGradientParam.m: Gradient of the Ordered categorical model's parameters.
orderedLikelihood.m: Likelihood of data under ordered categorical noise model.
orderedLogLikelihood.m: Log-likelihood of data under ordered categorical noise model.
orderedNoise3dPlot.m: Draw a 3D or contour plot for the probit.
orderedNoiseDisplay.m: Display the parameters of the ordered categorical noise model.
orderedNoiseExpandParam.m: Expand ordered categorical noise model's structure from param vector.
orderedNoiseExtractParam.m: Extract parameters from ordered categorical noise model.
orderedNoiseGradVals.m: Gradient wrt mu and varsigma of log-likelihood for ordered categorical noise model.
orderedNoiseGradientParam.m: Gradient of the ordered categorical noise model's parameters.
orderedNoiseOut.m: Output from ordered categorical noise model.
orderedNoiseParamInit.m: Ordered categorical noise model's parameter initialisation.
orderedNoisePointPlot.m: Plot the data-points for ordered categorical noise model.
orderedNoiseUpdateParams.m: Update parameters for ordered categorical noise model.
probitLikelihood.m: Likelihood of data under probit noise model.
probitLogLikelihood.m: Log-likelihood of data under probit noise model.
probitNoise3dPlot.m: Draw a 3D or contour plot for the probit.
probitNoiseDisplay.m: Display the parameters of the Probit noise model.
probitNoiseExpandParam.m: Expand probit noise structure from param vector.
probitNoiseExtractParam.m: Extract parameters from probit noise model.
probitNoiseGradVals.m: Gradient wrt mu and varsigma of log-likelihood for probit noise model.
probitNoiseGradientParam.m: Gradient of the probit noise model's parameters.
probitNoiseOut.m: Output from probit noise model.
probitNoiseParamInit.m: probistic classification model's parameter initialisation.
probitNoisePointPlot.m: Plot the data-points for probit noise model.
