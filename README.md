
# Paper-Writing

=============================================
* This new branch is to be used for analysing data from 2017 test beam. 
* The code runs with the one layer data, and will need (major) updates when we will have more layers. 
* This readme assumes one layer data.
* The README.md in other branches contain useful information about 2016 test beam analysis which might be still useful.

## The Paper structure

### fcc_hcal.tex
This is the file for summarize topics and combine them, the combining files include:<br />
* fcc_jets.tex<br />
* fcc_Mass_soft_drop_for_paper.tex<br />
* fcc_efficiency_and_Mann_after_mass_cut_for_paper.tex<br />

=============================================
### fcc_jets.tex
This part is from Dr.Sergei.<br />

=============================================
### fcc_Mass_soft_drop_for_paper.tex 
#### This part include soft drop mass at beta=0 and beta=2 
<ul>
<li>For histograms
<ul>
<li>All histograms include underflow and overflow number in the bin 1 and the last bin.</li>
<li>We choose __cluster__ to be our sample and do the analysis.</li>
<li>Now we will put all the FIGs in the paper, and we will select some of them to be the representations, and remove others later.</li>
</ul>
</li>
</ul>
* For histograms:<br />
 *  All histograms include underflow and overflow number in the bin 1 and the last bin.<br />
 *  We choose **cluster** to be our sample and do the analysis.<br />
 *  Now we will put all the FIGs in the paper, and we will select some of them to be the representations, and remove others later.<br />
<br />
* For analysis:<br />
 *  We use the median bin from signal, and fix at that bin **Right side** to be the central, and change the width to plot the ROC curves.<br />

>For summary:<br /> 
* We can find that in mass soft drop at beta=0 can separate signal and background perfectly up to center-of-mass at 20TeV in the smallest detector cell size. Upper to that, both of tt and ww can't be distinguished by smallest detector cell size.<br />
*For beta=2, there are no improvement in all center-of-mass energies when detector cell size is smallest.<br />
* **
=============================================
### fcc_efficiency_and_Mann_after_mass_cut_for_paper
#### This part include Tau21,Tau32,C2b1, and MannWhitney U test
* For histograms:<br />
 *  All histograms include underflow and overflow number in the bin 1 and the last bin.<br />
 *  After selecting with Prof.Ashutosh, we chose 0.5GeV cut (exclude cluster and 0.25GeV) for summary, both for ROC curves and MannWhitney U test.<br />
 *  In the FIGs, inclunding the histigrams of signal and background, MannWhitney value.<br />

* For analysis:<br />
 *  It has many steps as following:<br />
 (1)By the paper from Professor Jesse Thaler from MIT-->([The recursive soft drop](https://link.springer.com/content/pdf/10.1007%2FJHEP06%282018%29093.pdf))<br />
  He suggested us to cut the mass at signal 50%, so the first step, we cut the mass.<br />
 (2)From pearson lemma, it told us that use the ratio bin content to select the width, it can give us the best ROC curves, so the second one, we draw the ratio histogram, and we find the highest ratio histogram bin content to be the first bin.<br />
 (3)And we compare the left and the right ratio bin content, the higher side we will add that side to be the next one width. <br />
  For example, if the 15th bin has the highest ratio bin content, we will compare 14th and 16th, if 14th is higher than we will add 14th to be the next width, so our next width is [14th,15th], and so on. ( I will add some special condition and our setting ).

* For MannWhitney test, remembering that when the number close to zero, it means the distinguish power is better.<br />

>For summary:<br />
* There are no improvement in all variables in the smallest detector cell size. In some of variables, the biggest detector cell size is the best. This is an inetresting condition.<br />


