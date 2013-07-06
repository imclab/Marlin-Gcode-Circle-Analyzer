Marlin Gcode Circle Analyzer

A node.js script for analyzing Marlin-style Gcode for circular consistency.

Requires a series of Marlin-style Gcode instructions, creating a full circle.  The script then averages them to approximate a circle center, then measures the distance of all points from this center, averages those distances, and records the variance and standard deviation of those points from the circle.

Was originally conceived to see if there was a pattern to the circular deviation I was experiencing with my Reprap.  While there was some strangely sporadic deviance, it wasn't consistent enough to explain what I was observing.  Just the same, I'm saving it here for posterity and to help explain my Reprap situation to others.

Usage:
`node app.js gcode_file_name

Sample output (running 'gcode9'):
	$ node app.js gcode9
	Average: 12.016290723694608
	Variance: 0.018450236586620185
	Variance: 0.019052492734818172
	Variance: 0.01857611960306957
	Variance: 0.017064736465025442
	Variance: 0.017086656492903852
	Variance: 0.01658266183798858
	Variance: 0.01451955983872363
	Variance: 0.013601608381764123
	Variance: 0.01235145502007436
	Variance: 0.010468943974835498
	Variance: 0.010145491935974438
	Variance: 0.009360392510023987
	Variance: 0.008073169312961799
	Variance: 0.00636057781686404
	Variance: 0.0054818889101417205
	Variance: 0.003847249137303709
	Variance: 0.0033427090029396886
	Variance: 0.002378869374311499
	Variance: 0.0012607450714095612
	Variance: 0.0006120172786676726
	Variance: 0.0004612185987111843
	Variance: 0.0001482276297884715
	Variance: 0.00000908346832663633
	Variance: 0.00011457434346206358
	Variance: 0.0002680358623665568
	Variance: 0.0009373752037781363
	Variance: 0.0010108655952678462
	Variance: 0.0017709238358744066
	Variance: 0.002294186083156597
	Variance: 0.003393806576506534
	Variance: 0.004781554730608755
	Variance: 0.005515608506096662
	Variance: 0.0064644432062683005
	Variance: 0.007852150523766574
	Variance: 0.009590310411371157
	Variance: 0.01022404326490021
	Variance: 0.010988297944705138
	Variance: 0.012713485423380121
	Variance: 0.013418126631728087
	Variance: 0.01627622559827567
	Variance: 0.01582558797077633
	Variance: 0.017463884417239606
	Variance: 0.018432917689181372
	Variance: 0.017233076260054856
	Variance: 0.018919036490014175
	Variance: 0.016959801980507703
	Variance: 0.016263211000952092
	Variance: 0.01696204124911806
	Variance: 0.016373222212170378
	Variance: 0.016826870399468855
	Variance: 0.015051346882675036
	Variance: 0.01460750734505273
	Variance: 0.013000491131353282
	Variance: 0.011934021541525106
	Variance: 0.011321868081316131
	Variance: 0.011015758065770789
	Variance: 0.009081533332523876
	Variance: 0.0077431633206294665
	Variance: 0.006611206221592072
	Variance: 0.004801074233858726
	Variance: 0.0039292122747402215
	Variance: 0.003261478862416881
	Variance: 0.0017603274365829513
	Variance: 0.0012885131134471467
	Variance: 0.0007639310368100005
	Variance: 0.0004950302321403099
	Variance: 0.00020079939494981714
	Variance: 0.000004814565064705691
	Variance: 0.00003382233153230661
	Variance: 0.00013713125733399284
	Variance: 0.0005243990447772561
	Variance: 0.0011023409101679944
	Variance: 0.0018733454912982389
	Variance: 0.0023770571526576445
	Variance: 0.0032468502605263743
	Variance: 0.003967324793814637
	Variance: 0.005704731420742002
	Variance: 0.007251663915027879
	Variance: 0.008498491087502825
	Variance: 0.00936929539949028
	Variance: 0.00966919196283652
	Variance: 0.01128343128768361
	Variance: 0.012327114109492318
	Variance: 0.014315360409025002
	Variance: 0.015041651234181072
	Variance: 0.016220577305876647
	Variance: 0.01583188911277604
	Variance: 0.01732883833673783
	Variance: 0.017551774029019453
	Variance: 0.01753114182820126
	Standard deviation: 0.09405490560467532