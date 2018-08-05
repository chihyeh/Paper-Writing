
# Paper-Writing

* This is the structure for the paper.<br />
* Please don't hesitate to ask me any questions.<br />
* I will put all codes which are used in this study on the github later.<br />

You can download the files:
```bash
git clone https://github.com/chihyeh/Paper-Writing.git
```
in the terminal

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
#### This part includes soft drop mass at beta=0 and beta=2 
<ul>
<li>For histograms
<ul>
<li>All histograms include underflow and overflow number in the bin 1 and the last bin.</li>
<li>We choose <strong>CLUSTER</strong> to do the analysis and the histograms.</li>
<li>Now we put all FIGs in the paper, and we will select some of them to be the representations, removing others later.</li>
</ul>
</li>
</ul>

<ul>
<li>For analysis
<ul>
<li>We use the <strong>MEDIAN BIN</strong> from signal, and fix at that bin <strong>RIGHT SIDE</strong> to be the central value, and change the width to plot the ROC curves</li>
<li>We choose <strong>Cluster</strong> to do the analysis as before mention.</li>
</ul>
</li>
</ul>

For summary:
<ol>
<li>We can conclude that in soft drop method, beta=0 can separate signal and background perfectly up to center-of-mass at 20TeV in the smallest detector cell size. Bigger than that, both of tt and ww can't be distinguished from background by smallest detector cell size perfectly.</li>
<li>In beta=2, there is no improvement in all center-of-mass energies when detector cell size is smallest.</li>
</ol>

=============================================
### fcc_efficiency_and_Mann_after_mass_cut_for_paper
#### This part include Tau21,Tau32,C2b1, and MannWhitney U test
<ul>
<li>For histograms
<ul>
<li>All histograms include underflow and overflow number in the bin 1 and the last bin.</li>
<li>After selecting with Prof.Ashutosh, we choose 0.5GeV cut (exclude cluster and 0.25GeV) for summary, both for ROC curves and MannWhitney U test.</li>
<li>In the FIGs, inclunding the histigrams of signal and background, and MannWhitney value.</li>
</ul>
</li>
</ul>

<ul>
<li>For analysis
<ol>
<li>It has many steps as following
<ol>
<li>By the paper from Professor Jesse Thaler from MIT-->[The recursive soft drop](https://link.springer.com/content/pdf/10.1007%2FJHEP06%282018%29093.pdf)<br />
    He suggested us to cut the mass at signal 50%, so the first step, we cut at there.</li>
<li>From pearson lemma, it told us that use the ratio bin content to select the width, it can give us the best ROC curves, so the second one, we draw the ratio histogram, and we find the highest ratio histogram bin content to be the first bin.</li>
<li>And we compare the left and the right ratio bin content, the higher side we will add that side to be the next one width. For example, if the 15th bin has the highest ratio bin content, we will compare 14th and 16th, if 14th is higher than we will add 14th to be the next width, so our next width is [14th,15th], and so on. ( I will add some special condition and our setting ).</li>
</ol>
<li>For MannWhitney test, remembering that when the number close to zero, it means the distinguish power is better.</li>
</ul>

For summary: 
* There are no improvement in all variables in the smallest detector cell size. In some of variables, the biggest detector cell size is the best. This is an inetresting condition.<br />


