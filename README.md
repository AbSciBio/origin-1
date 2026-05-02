# Origin-1
This repository contains data generated as part of the study [Origin-1: a generative AI platform for _de novo_ antibody design against novel epitopes](https://www.absci.com/wp-content/uploads/2026/01/260114_Origin1_Final_Submission.pdf). _In silico_ and _in vitro_ data are included in this repository. Additional binding, developability, functionality, and structure confirmation results can be found in the paper.

-----------------------------------------------------------------------------------------------------
Data in `de_novo_spr_data.csv` are organized with the following columns:
* `Design`: Design identifier indicating target and rank (lower = higher rank)
* `Heavy Chain`: Heavy chain variable domain sequence
* `Light Chain`: Light chain variable domain sequence
* `Target`: Target antigen
* `Framework`: Therapeutic antibody used for framework scaffold
* `Epitope`: Epitope identifier
* `Binder`: Boolean indicating whether or not the design is a binder
-----------------------------------------------------------------------------------------------------
Data in `lead_optimization_spr_data.csv` are organized with the following columns:
* `Heavy Chain`: Heavy chain variable domain sequence
* `Light Chain`: Light chain variable domain sequence
* `Target`: Target antigen. We use AZGP1-A and AZGP1-B to both indicate screening against AZGP1 but that different parents were used for optimization.
* `Mutation`: Mutation made from parent sequence (e.g. H-S31A is an S to A mutation at 1-indexed position 31 of the heavy chain). NaN indicates the parent sequence.
* `Binder`: Boolean indicating whether or not the design is a binder. Note that a NaN may be present which indicates the respective antibody could not be measured for binding.
* `KD (nM)`: Dissociation constant in nM units
* `pKD`: Negative logarithm of dissociation constant
-----------------------------------------------------------------------------------------------------
Data in `round2_il36ra_lead_optimization_spr_data.csv` are organized with the following columns:
* `Heavy Chain`: Heavy chain variable domain sequence.
* `Light Chain`: Light chain variable domain sequence.
* `Mutations`: Mutations made from parent sequence (e.g. H-S31A is an S to A mutation at 1-indexed position 31 of the heavy chain).
* `Number of Mutations`: Number of mutations made from parent sequence.
* `Target`: Target antigen, in this case IL36RA.
* `Human Binder`: Boolean indicating whether or not the design is a binder in human cells. 
* `Human KD (nM)`: Dissociation constant in nM units.
* `Human pKD`: Negative logarithm of dissociation constant.
* `Mouse Binder`: Boolean indicating whether or not the design is a binder in mouse cells. 
* `Mouse KD (nM)`: Dissociation constant in nM units.
* `Mouse pKD`: Negative logarithm of dissociation constant.
-----------------------------------------------------------------------------------------------------
Data in `round2_col6a3_lead_optimization_spr_data.csv` are organized with the following columns:
* `Heavy Chain`: Heavy chain variable domain sequence.
* `Light Chain`: Light chain variable domain sequence.
* `Mutations`: Mutations made from parent sequence (e.g. H-S31A is an S to A mutation at 1-indexed position 31 of the heavy chain).
* `Number of Mutations`: Number of mutations made from parent sequence.
* `Target`: Target antigen, in this case COL6A3.
* `Binder`: Boolean indicating whether or not the design is a binder. 
* `KD (nM)`: Dissociation constant in nM units.
* `pKD`: Negative logarithm of dissociation constant.
* `note`: Note relevant for interpreting result.
-----------------------------------------------------------------------------------------------------
The `abscibind` and `abscigen` folders contain the computational models generated for the reported designs by AbsciBind and AbsciGen, respectively.

# Citations
If you find these data or results useful, we ask that you cite our work:
```
@article{Levine2026Origin1,
  title = {Origin-1: a generative AI platform for de novo antibody design against novel epitopes},
  author = {Levine, Simon and King, Jonathan Edward and Stern, Jacob and Grayson, David and Wang, Raymond and Yin, Rui and Lupo, Umberto and Kulytė, Paulina and Brand, Ryan Matthew and Bertin, Tristan and Pfingsten, Robert and Cejovic, Jovan and Chung, Chelsea and Luton, Breanna K. and Hagemann, Andrew and Haile, Robel and Medina, Elliot and Panwar, Pankaj and Dubrovskyi, Oleksii and LaCombe, Chase and Anderson, Zahra and Mildh, Derrik and Benjamin, Scott and Kaiser, Joe and Ferron, Joseph and Sarrico, Marta and Kershner, Alexandria and Mishra, Apurva and Ejan, Kai R. and Marsh, Emily K. and Bringas, Paul and Vilaychack, Phetsamay and Chapman, Kyra and Ripley, Jacob and Gowda, Muttappa and Collins, Kathryn M. and McCloskey, Cailen M. and Joseph, Jeremiah S. and Ripley, Rylee and Abdulhaqq, Shaheed A. and Feltner, Audree and Guerin, Michael and Goby, Jeffrey and Hendricks, Jesse and Castillo, Danielle and McClain, Sean and Ganini, Douglas and Shpiel, Derek and Mategko, James and Garcia, Eder Cruz and Zabet-Moghaddam, Masoud and Sutton, John M. and Guo, Zheyuan and West, Sean M. and Iyer, Janani S. and Shanehsazzadeh, Amir},
  year = {2026},
  journal = {bioRxiv},
  doi = {10.64898/2026.01.14.699389},
  url = {https://www.biorxiv.org/content/10.64898/2026.01.14.699389v1}
}
```
