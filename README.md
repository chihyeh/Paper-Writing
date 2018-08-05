
# Paper-Writing

* This is the structure of the paper.<br />
* Please don't hesitate to ask me any questions.<br />
* I will put all codes which are used in this study on the github later.<br />

You can download the files:
```bash
git clone https://github.com/chihyeh/Paper-Writing.git
```
in the terminal

## The Paper structure

### fcc_hcal.tex
This is the file for summarizing topics and combine them, the combining files include:<br />
* fcc_jets.tex<br />
* fcc_Mass_soft_drop_for_paper.tex<br />
* fcc_efficiency_and_Mann_after_mass_cut_for_paper.tex<br />

=============================================
### fcc_jets.tex
This part is from Dr.Sergei.<br />

=============================================
### fcc_Mass_soft_drop_for_paper.tex 
#### This part includes soft drop mass at beta=0 and beta=2 
<ul>
<li>For histograms
<ul>
<li>All histograms include underflow and overflow number in the bin 1 and the last bin.</li>
<li>We choose <strong>CLUSTER</strong> to do the analysis and the histograms.</li>
<li>Now we put all Figures in the paper, and we will select some of them to be the representations, removing others later.</li>
</ul>
</li>
</ul>

<ul>
<li>For analysis
<ul>
<li>We use the <strong>MEDIAN BIN</strong> from signal, and fix at that bin <strong>RIGHT SIDE</strong> to be the central value, and change the width to plot the ROC curves</li>
<li>We symmetrically add the bins from the central value ( every time we add two bins, and totally add 14 bins to be our width).
</ul>
</li>
</ul>

For summary:
<ol>
<li>We can conclude that in soft drop method, beta=0 can separate signal and background <strong>PERFECTLY up to 20 TeV center-of-mass energy</strong> in the smallest detector cell size. Bigger than that, both of tt and ww can't be distinguished from qq by smallest detector cell size perfectly.</li>
<li>In beta=2, there is <strong>NO IMPROVEMENT</strong> in all center-of-mass energies when detector cell size is smallest.</li>
</ol>

=============================================
### fcc_efficiency_and_Mann_after_mass_cut_for_paper
#### This part include Tau21,Tau32,C2b1, and MannWhitney U test
<ul>
<li>For histograms
<ul>
<li>All histograms include underflow and overflow number in the bin 1 and the last bin.</li>
<li>After selecting with Prof.Ashutosh, we choose <strong>0.5GEV CUT</strong>(exclude cluster and 0.25GeV) for summary, both for ROC curves and MannWhitney U test.</li>
<li>In the FIGs, inclunding the histigrams of signal and background, and MannWhitney value.</li>
</ul>
</li>
</ul>

<ul>
<li>For analysis
<ol>
<li>There have many steps as following
<ol>
<li>By the paper from Professor Jesse Thaler from MIT-->[The recursive soft drop](https://link.springer.com/content/pdf/10.1007%2FJHEP06%282018%29093.pdf)<br />
    He suggested us to cut the mass at signal 50%, so the first step, we cut at there.</li>
<li>From pearson lemma, it told us that using the ratio bin content <strong>[SIG/BKG]</strong> to select the width, it can give us the best ROC curve, so the second one, we draw the ratio histogram, and we find the highest ratio bin content to be the first bin and draw the ROC curves.</li>
<li>We compare left and right ratio bin content from the highest ratio bin content, We will add the higher side to be our next width, and keep comparing left and right ratio bin content out of the next width. For example:
<ol>
<li>[ath,bth] means [ath bin to bth bin]==>[14th,16th] means 14th,15th,16th.
<li>if the 15th bin has the highest ratio bin content, we will compare 14th and 16th, if 14th is higher than 16th, we will add 14th to be the next width, so our next width is [14th,15th].</li>
<li>Next, because our new width is [14th,15th], so we need to compare the ratio bin content about 13th and 16th, if 16th is higher than 13th, we will add the width to [14th,16th], and so on.</li>
<li>There have some special cases when we do and compare the ratio histogram bin, I will talk some <strong>special conditions and our settings</strong> in PS.</li>
</ol>
</ol>
<li>For MannWhitney test, remembering that when the number close to zero, it means the distinguish power is better.</li>
</ul>

For summary: 
* There are <strong>no improvement</strong> in all variables in the smallest detector cell size. In some of variables, the biggest detector cell size is the best. This is an inetresting condition.<br />
<br />
<br />

<ul>
<li>PS: Detail about the analysis in Tau and C variables (A little bit complicated)
<ul>
<li>In the default ratio bin content, we use <strong>[SIG/BKG]</strong> in root "Divide" function [bin by bin], but we found that when SIG bin content!=0 and BKG bin content=0, that bin's ratio bin content is zero in default. But in the math, if !0/0, we can find the extreme value, so we set an extreme value manually when SIG bin content!=0 and BKG bin content=0 happen. All other ratio bin contents are same as default.</li>
<br />
<li>When we compare left and right ratio bin content, in some conditions, we could bump into the ratio bin content is zero in the certain side (or both sides), and we set other value to represent this ratio bin content. In general, we use the signal and background bins before ( when this bin is left ) or after ( when this bin is right ) this ratio bin content. The formula is Signal/background of the Integral value, I will give an example later.
<ul>
<li>Now, supposing that our width now is [14th,15th], we want to compare 13th with 16th.</li>
<li>If the left ratio bin content is zero (13th bin) in default, we will see two things : Integral.[Minimum bin number=1th in our study, 12th] of SIG and BKG, and using the setting value to represent this ratio bin content.
<ol>
<li>If SIG.Integral[1th,12th] = 0 , BKG.Integral[1th,12th]= 0 ==> We will set the ratio bin content as -1 [13th ratio bin content=-1], and let it continually add other side until both side are no signal and background.</li> 
<li>If SIG.Integral[1th,12th] != 0 , BKG.Integral[1th,12th]= 0 ==> We will set the ratio bin content as 9999[13th ratio bin content=9999], and let it continually add this side until this side have no signal.</li> 
<li>If SIG.Integral[1th,12th] = 0 , BKG.Integral[1th,12th] != 0 ==> Just like the ratio bin content formula, signal/background=0[13th ratio bin content=0]</li> 
<li>If SIG.Integral[1th,12th] != 0 , BKG.Integral[1th,12th] != 0 ==> Just like the ratio bin content formula, signal/background=the value it have[13th ratio bin content=the value it have]</li> 
</ol>
<li>If the right ratio bin content is zero (16th bin) in default, we will see two things : [17th,Maximum bin number=25th in our study] SIG and BKG.
<ol>
<li>If SIG.Integral[17th,25th] = 0 , BKG.Integral[17th,25th] = 0 ==> We will set the ratio bin content as -1[16th ratio bin content=-1], and let it continually add other side until both side are no signal and background.</li> 
<li>If SIG.Integral[17th,25th] != 0 , BKG.Integral[17th,25th] = 0 ==> We will set the ratio bin content as 9999[16th ratio bin content=9999], and let it continually add this side until this side have no signal.</li> 
<li>If SIG.Integral[17th,25th] = 0 , BKG.Integral[17th,25th] != 0 ==> Just like the ratio bin content formula, signal/background=0[16th ratio bin content=0]</li> 
<li>If SIG.Integral[17th,25th] != 0 , BKG.Integral[17th,25th] != 0 ==> Just like the ratio bin content formula, signal/background=the value it have[16th ratio bin content=the value it have]</li> 
</ol>

</ul>
<li>If left and right have same ratio bin content, we will randomly choose one side to add.</li>
<li>Comparing all the bins, we can fninish drawing the ROC curves.</li>
</li>
</li>
</ul>






