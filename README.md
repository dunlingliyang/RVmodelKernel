RV model-based kernel with LSM
==============================
This repository contains the source code for classification based on the liquid state machine (LSM for short).

We build our project on the basis of codes provided by Fengzhen Tang (fxt126@cs.bham.ac.uk). This repository integrates many codes from other literatures and all the contact information is retained in the preamble. *ALL* necessary codes can be obtained  *freely* from the Internet.

Run `RV model-based kernel/demo.m` to view the demo result.

### HOWTO

+ How to start?
	* download the data sets from website [here](http://www.cs.ucr.edu/~eamonn/time_series_data/) (The data sets are not included in this repo.)
    * __run `initpath` firstly__.
    * run `NormalRV`, `GMMRV`, `fisherRV`, `SamplingRV` to test classification.
    * run `demo.m`, also show the classification results.
+ How to adjust reservoir size (R_no) and regression coefficient (val) to get a best fitting?
    * You can run `lsm_weight_*.m` directly to see the fitting error, and write your own script to adjust the `R_no` and `val`.
    * Use the `test/test.m` to find best choice of `R_no` and `val`.
    * Also, the default settings in `test/test.m` are good tutorial for you.
+ How to adjust svm parameters in svm, i.e. `cost` and `kp`?
    * Run `NormalRV`, `GMMRV`, `fisherRV`, `SamplingRV` by inputing a list of `cost` and `kp`, they will return the best classification accuracy.

### Dependencies Version

This repository includes a precompiled version of `csim 1.1.1` and `libsvm 3.2`, including mexw64, mexa64m, mexmaci64 for usage under Windows, Linux, Mac.

The csim can be found [here](https://git.ustclug.org/snn/csim). N.B. the original version from the website was altered to meet the updated environment.

__libsvm 3.2__ or higher version is required. __libsvm__ is a library for support vector machines which can be found [here](http://www.csie.ntu.edu.tw/~cjlin/libsvm/).
s

### About

This repository is created by Junyuan Hong(jyhong836@gmail.com), and contributed by Junyuan Hong and [Yang Li](http://home.ustc.edu.cn/~csly).

