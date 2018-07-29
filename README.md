# Paper-Writing

=============================================<br />
You can download files:<br />
git clone https://github.com/chihyeh/Paper-Writing.git 
in your terminal.

*This is the structure for the paper.<br />
*Please don't hesitate to ask me any questions.<br />


## The Paper structure

### fcc_hcal.tex
This is the file for summarizeall topics and combine them, including:<br />
*fcc_jets.tex<br />
*fcc_Mass_soft_drop_for_paper.tex<br />
*fcc_efficiency_and_Mann_after_mass_cut_for_paper.tex<br />\

=============================================
### fcc_jets.tex
This part is from Dr.Sergei.<br />

=============================================
### fcc_Mass_soft_drop_for_paper.tex <br />
#### This part include soft drop mass at beta=0 and beta=2 <br \>
*For the histograms, because we want to include 99% signal, we just choose the range that includes them, and processes are in the figure also.<br />
*For analysis, we use the median bin from signal, and fix at that bin **Right side** to be the central, and change the width to plot the ROC curves.<br />

#### For summary: 
we can find that in mass soft drop at beta=0 can separate signal and background perfect up to 20TeV in the smallest detector cell size. Upper to that, both of tt and ww can't be distinguished by smallest detector cell size.<br />
For beta=2, there is no improvement in all energies when detector cell sizes is smallest.<br />

=============================================
### fcc_efficiency_and_Mann_after_mass_cut_for_paper
#### This part include Tau21,Tau32,C2b1, and MannWhitney U test <br /> 
After selecting with Prof.Ashutosh, we chose 0.5GeV cut (exclude cluster and 0.25GeV) for summary, both for ROC curves and MannWhitney U test.<br />
*For MannWhitney test, remembering that when the number close to zero, it means the distinguish power is better.
