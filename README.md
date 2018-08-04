
# Paper-Writing

color.Println(color.BlackBg("_black background_", color.Wht))
[Visit GitHub!](www.github.com)

=============================================<br />
You can download files:<br />
git clone https://github.com/chihyeh/Paper-Writing.git <br />
in your terminal.

*This is the structure for the paper.<br />
*Please don't hesitate to ask me any questions.<br />
*I will put all codes which are used in this study on the github later.<br />


## The Paper structure

### fcc_hcal.tex
This is the file for summarize topics and combine them, including:<br />
*fcc_jets.tex<br />
*fcc_Mass_soft_drop_for_paper.tex<br />
*fcc_efficiency_and_Mann_after_mass_cut_for_paper.tex<br />

=============================================
### fcc_jets.tex
This part is from Dr.Sergei.<br />

=============================================
### fcc_Mass_soft_drop_for_paper.tex 
#### This part include soft drop mass at beta=0 and beta=2 
*For histograms:<br />
 *All histograms include underflow and overflow number in the bin 1 and the last bin.<br />
 *We choose **cluster** to do the analysis and the histograms we will use.<br />
 *Now we will put all the FIGs in the paper, and we will select some of them to be the representations, and remove others later.<br />
<br />
*For analysis:<br />
 *We use the median bin from signal, and fix at that bin **Right side** to be the central, and change the width to plot the ROC curves.<br />

#### For summary: 
*We can find that in mass soft drop at \beta=0 can separate signal and background perfectly up to 20TeV in the smallest detector cell size. Upper to that, both of tt and ww can't be distinguished by smallest detector cell size.<br />
*For beta=2, there is no improvement in all energies when detector cell size is smallest.<br />

=============================================
### fcc_efficiency_and_Mann_after_mass_cut_for_paper
#### This part include Tau21,Tau32,C2b1, and MannWhitney U test 
*All histograms include underflow and overflow number in the bin 1 and the last bin.
After selecting with Prof.Ashutosh, we chose 0.5GeV cut (exclude cluster and 0.25GeV) for summary, both for ROC curves and MannWhitney U test.<br />
*For analysis, it has many steps:
By the paper from Professor Jesse Thaler from MIT <https://link.springer.com/content/pdf/10.1007%2FJHEP06%282018%29093.pdf>, he suggested us to cut the mass at signal 50%, so the first step, we cut at there.

The second one, from pearson lemma, it told us that use the ratio bin content to select the width, it can give us the best ROC curves, so the second one, we draw the ratio histogram, and 
*For MannWhitney test, remembering that when the number close to zero, it means the distinguish power is better.
