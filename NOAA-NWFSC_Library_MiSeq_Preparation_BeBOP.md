---
# MIOP terms
methodology_category: Omics Analysis
project: NOAA NWFSC Cook Inlet Beluga Whale
purpose: PCR [OBI:0000415], Library Preparation [OBI:0000711]
analyses: PCR [OBI:0000415], Library Preparation [OBI:0000711]
geographic_location: Cook Inlet [GAZ:00051076], Turnagain Arm [GAZ:00051080], Kenai River [GAZ:00197390]
broad_scale_environmental_context: marine biome [ENVO:00000447], marine photic zone [ENVO:00000209], freshwater biome [ENVO:00000873]
local_environmental_context: oceanic epipelagic zone biome [ENVO:01000035], marine benthic biome [ENVO:01000024], freshwater river [ENVO:01000297], estuary [ENVO:00000045]
environmental_medium: ea water [ENVO:00002149], fresh water [ENVO:00002011]
target: amplicon sequencing assay [OBI_0002767]
creator: Zachary Gold
materials_required: vortexer [OBI:0400118], PCR instrument [OBI:0000989], Centrifuge [OBI:0400106]
skills_required: 'sterile technique, pipetting skills, standard molecular technique'
time_required: 300
personnel_required: 1
language: en
issued: '2026-5-07'
audience: 'scientists'
publisher: 'NOAA Pacific Marine Environmental Laboratory Ocean Molecular Ecology Group; University of Washington Cooperative Institute for Climate, Ocean, & Ecosystem Studies'
hasVersion: 1.0.0
license: CC0 1.0 Universal
maturity level: mature

# FAIRe terms
barcoding_pcr_appr: two-step pcr
pcr2_amplificationReactionVolume: 25
pcr2_commercial_mm: NEB Phusion High Fidelity Master Mix
pcr2_dna_vol: 5
pcr2_cond: initial denaturation:95_5; denaturation:98_0.33; annealing:56_0.5; elongation:72_3;8;final extension:72_5;
pcr2_annealingTemp: 55
pcr2_cycles: 8
pcr2_analysis_software: 'missing: not collected'
pcr2_plate_id: 'missing: not collected'
pcr2_method_additional: 'missing: not collected'
sequencing_location: NOAA NWFSC Conservation Biology Division
platform: Illumina
instrument: Illumina MiSeq
seq_kit: Illumina MiSeq V3 PE 2x300bp  (Cat_No:MS-102-3003)
lib_layout: paired end
lib_screen: 'PCR1 product was purified and size selected using an Ampure XP bead cean up before PCR2, then barcoded using two-step barcoding PCR with Illumina Nextera Unique Dual Indices, purified and size selected using an Ampure XP bead clean up,  normalized with Life Technologies SequalPrep Normalization kit, pooled using 10 µL of product and diluted to 6 pM with 20% PhiX before loading it onto a MiSeq Flow Cell'
adapter_forward: TCGTCGGCAGCGTCAGATGTGTATAAGAGACAG
adapter_reverse: GTCTCGTGGGCTCGGAGATGTGTATAAGAGACAG
lib_conc: 6
lib_conc_unit: pM
lib_conc_meth: Qubit
phix_perc: 20
checksum_method: linux md5sum
seq_method_additional: PhiX was spiked in at 20%
demux_tool: 'MiSeq Instrument'
demux_max_mismatch: '0'
---
# NOAA NWFSC Metabarcoding Library Preparation Protocol 

## PROTOCOL INFORMATION

### Minimum Information about an Omics Protocol (MIOP)

- MIOP terms are listed in the YAML frontmatter of this page.
- See <https://github.com/BeBOP-OBON/miop/blob/main/model/schema/terms.yamL> for the list and definitions.

### Making eDNA FAIR (FAIRe)

- FAIRe terms are listed in the YAML frontmatter of this page.
- See <https://fair-edna.github.io/download.htmL> for the FAIRe checklist and more information.
- See <https://fair-edna.github.io/guidelines.htmL#missing-values> for guidelines on missing values that can be used for missing FAIRe or MIOP terms.

### Authors

| PREPARED BY | AFFILIATION | ORCID | DATE |
| ------------- | ------------- | ------------- | ------------- |
| Zachary Gold	|Ocean Molecular Ecology, NOAA PMEL	|<http://orcid.org/0000-0003-0490-7630>	|2025-05-01|

### Related Protocols

- This section contains protocols that should be known to users of this protocol.
- Include the link to each protocol.
- Include the version number and release date (if available).
- Internal/External: "Internal" are derivative or altered protocols, or other protocols in this workflow. "External" are protocols from manufacturers or other groups.

| PROTOCOL NAME | LINK         | VERSION      | RELEASE DATE | INTERNAL/EXTERNAL |
| ------------- | ------------ | ------------ | ------------ | ----------------- |
|NOAA-PMEL-OME MiFish mod Universal Teleost 12S PCR Protocol | https://github.com/marinednadude/NOAA-PMEL-OME-MiFish-mod-Universal-Teleost-12S-PCR-Protocol-BeBOP/blob/main/NOAA-PMEL-OME-MiFish-mod-Universal-Teleost-12S-PCR-Protocol-BeBOP.md |1.2.1| 2025-11-14| Internal |

### Protocol Revision Record

| VERSION | RELEASE DATE | DESCRIPTION OF REVISIONS |
| ------------- | ------------- | ------------- |
| 1.0.0 | 2026-05-07 | Initial release |

### Acronyms and Abbreviations

| ACRONYM / ABBREVIATION | DEFINITION |
| ------------- | ------------- |
|BSC|Biosafety cabinet|
|CICOES| Cooperative Institute for Climate, Ocean, & Ecosystem Studies|
|dNTP	|deoxynucleotide triphosphate|
|eDNA	|environmental DNA|
|EtOH| Ethanol|
|NOAA |National Oceanic and Atmospheric Administration|
|OME	|Ocean Molecular Ecology |
|PCR| Polymerase chain reaction |
|PMEL	|Pacific Marine Environmental Laboratory|
|PPE | Personal protective equipment |
|UW| University of Washington|
| UDI | Unique Dual Index |

### Glossary

| SPECIALISED TERM | DEFINITION |
| ------------- | ------------- |
| Library | A collection of DNA fragments that have been prepared (cleaned, indexed, and adapter-ligated) for sequencing.|
| Pooling | The process of combining multiple indexed libraries into a single tube at equal molar ratios. |

## BACKGROUND

### Summary

This protocol is used by NOAA NWFSC to prepare next-generation amplicon/metabarcoding sequencing libraries from PCR1 products. Metabarcoding was performed on all eDNA samples using a previously published two-step PCR library preparation method (Curd et al., 2019; Gold et al., 2021, 2022). PCR1 products are cleaned using Ampure XP beads (Beckman Coulter, CA, USA) prior to indexing. DNA libraries are generated using indexes from the Nextera Unique Dual Index A through D Kits (Illumina, CA, USA). PCR2 indexing was performed using a 25 μL reaction mixture containing 12.5 μL of NEB Phusion High-Fidelity PCR Master Mix (New England Biosystems, MA, USA), 0.625 μL of primer i7, 0.625 μL of primer i5, and 5 ng of PCR 1 template. We electrophoresed all indexed PCR products on 2% agarose gels to confirm correct product size. Indexed PCRs were normalized using a SequalPrep Normalization Plate Kit (ThermoFisher, MA, USA) and then pooled in equimolar concentration. The final pool was cleaned and concentrated using Ampure XP beads. Library size was confirmed on an Agilent TapeStation (Agilent, CA, USA). Samples were organized into 5 distinct sequencing runs conducted on a MiSeq using Reagent Kit V3 PE 2x300bp at NWFSC, using loading 6pM of the library with 20% PhiX.


This protocol has been used over multiple years and has evolved over time.

### Method Description and Rationale

Advantages of this protocol include ease of use, the ability to leverage commercially available Illumina sequencing kits and indices, and the ability to use any PCR1 locus. This protocol's steps include: _PCR Amplicon Cleanup_, _Barcoding/Indexing PCR_, _PCR Normalization and Pooling_, and _Sequencing_. 

eDNA sample collection, filtration, extraction, and PCR amplification before this protocol. PCR1 product is first cleaned to remove excess primers and dNTPs using an Ampute XP bead clean up. The cleaned PCR product is then indexed through a second barcoding PCR step using Illumina Nextera UDI indices. Indexed PCR2 product is then cleaned again using the above bead cleaning steps before being normalized using SequalPrep Normalization Plates (Life Technologies, Carlsbad, CA) and then pooled by even volume (and concentration) into a final pooled library. The library is diluted to 6 pM with 20% PhiX spike in. The library is then sequenced on an Illumina Miseq  using the MiSeq Reagent Kit V3 2x300 bp. The MiSeq instrument demultiplexes raw sequence data.


### Spatial Coverage and Environment(s) of Relevance

This protocol can be used for library preparation of any marker gene region for metabarcoding.

### Personnel Required

One person with molecular biology experience.

### Safety

This protocol uses bleach and ethanol, both of which are classified as hazardous chemicals. Appropriate PPE must be worn, and standard safety procedures should be followed to avoid skin and eye exposure.

### Training Requirements

Molecular biology training (including, at a minimum, sterile technique, pipetting small volumes, and programming and running PCR thermocyclers) is required to conduct this protocol.

### Time Required to Execute the Procedure

This protocol takes about 4-5 hours to execute per plate. There is a safe-stopping point after the PCR Amplicon Cleanup, Indexing PCR, Normalization, and Pooling steps. Across all stopping points, the plate can be stored for up to a week at 4°C, with storage at -20˚C for up to 6 months.

## EQUIPMENT

| DESCRIPTION | PRODUCT NAME AND MODEL | MANUFACTURER | QUANTITY | REMARK |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| **Durable equipment** |
| Thermal Cycler | Mastercycler Nexus Thermal Cycler | Eppendorf | 1 | Can be substituted with generic |
| Vortex | Vortex Genie | Scientific Industries | 1 | Can be substituted with generic |
| PCR plate centrifuge | Microplate centrifuge | Generic | 1 | |
| Magnetic separator | 96-Well magnetic separator | Generic | 1 | |
| Pipettor: 0.5-10 μL | Research plus adjustable-volume pipette | Eppendorf | 1 | Can be substituted with any accurate pipette. |
| Pipettor: 100-1000 μL | Research plus adjustable-volume pipette | Eppendorf | 1 | Can be substituted with any accurate pipette. |
| Pipettor: 10-100 μL |  Research plus adjustable-volume pipette | Eppendorf | 1 | Can be substituted with any accurate pipette. |
| Multi-channel pipettor: 10-100 μL | Research plus 8-channel pipette | Eppendorf | 1 | Can be substituted with any accurate pipette. |
| Multi-channel pipettor: 0.5-10 μL | Research plus 8-channel pipette | Eppendorf | 1 | Can be substituted with any accurate pipette. |
| Serological pipette | Easypet 3 pipette | Eppendorf | 1 | Can be substituted with any accurate pipette.|
| PCR cooler rack | PCR cooler 0.2-0.5 mL | Eppendorf | 1 | Can be substituted with generic|
| Ice bucket | Generic | Generic | 1 | |
| **Consumable equipment** |
| 96-well PCR plate | Armadillo PCR plate, 96-well, clear wells | ThermoFisher | 2 | Can be substituted with generic. |
| Aluminum foil sealing tape | AlumaSeal II sealing foils for PCR and cold storage | VWR | 7 | Can be substituted with generic. | 
| 8-Strip tubes | 0.2 mL 8-strip PCR tubes | Generic | 5 |  |
| Microcentrifuge tubes | 2.0 mL microcentrifuge tube | Generic | 8 | |
| 200 μL pipette tips  | Filter tips 200 μL graduated| Generic | 4 | Must be sterile and filtered. |
| 10 μL pipette tips  | Filter tips 10 μL graduated | Generic | 96 | Must be sterile and filtered. |
| 25 mL Trough | Reagent reservoirs - 25 mL disposable | ThermoFisher Scientific | 1 box | Can be substituted with generic. |
| Gloves | Nitrile gloves | Generic | 1 box | |
| Kimwipes | Delicate task wipes | KimTech | 1 box | Can be substituted with generic; must be lint-free. |
| **Chemicals** |
| 100% and 70% EtOH | Molecular biology grade ethanol |
| 10% bleach| Hypochlorite bleach |Clorox|  |  |
| Nuclease-free water | Nuclease-free water (not DEPC-Treated) | ThermoFisher Scientific | 1 | (mL vial) |
| Illumina Unique Dual Indexes Sets A, B, C, D | Illumina Unique Dual Indexes| Illumina | 1 | Illumina® DNA/RNA UD Indexes Set A, Tagmentation (96 Indexes, 96 Samples) 20091654; Illumina DNA/RNA UD Indexes Set B, Tagmentation (96 Indexes, 96 Samples) 20091656; Illumina® DNA/RNA UD Indexes Set C, Tagmentation (96 Indexes, 96 Samples) 20091658; Illumina® DNA/RNA UD Indexes Set D, Tagmentation (96 Indexes, 96 Samples) 20091660 |
| Promega Master Mix | Premixed 2X solution of Taq DNA Polymerase, dNTP,s and Reaction Buffer | Promega | 1 | (kit) Master Mix includes Taq DNA polymerase, dNTPs, MgCl2, and reaction buffer |
| Ampure XP beads | Ampure XP Magnetic Beads | Cytiva | 1 | (10 mL) |
| SequalPrep Normalization Kit | SequalPrep Normalization Plate Kit, 96-wells | Applied Biosystems | 10 | Cat No: A1051001 |
| Illumina MiSeq V3 PE 2x300bp (300 cycles)   | Includes one SP flow cell, one buffer cartridge, one cluster cartridge, and one sequencing cartridge to support a 300-cycle run on the MiSeq System. | Illumina | 1 | (flow cell) Cat_No:MS-102-3003 |

## STANDARD OPERATING PROCEDURE

### Protocol

#### Preparation

1. Sterilize workspaces and durable equipment, including pipettes within the BSC, with 10% bleach. Then wipe down all surfaces and equipment with 70% EtOH.
2. If you have a UV crosslinker available, UV pipettes and tube racks regularly for 2 minutes. 
3. Run the UV light in the BSC for 30 minutes before starting work.
4. Label all PCR plates both on the side of the plate and on the top of the foil (in the plate margins). Recommended labeling scheme includes plate name, primer, date of PCR, and personnel initials.

#### PCR1 Cleanup (Bead Clean)

PCR1 products were first cleaned by using an Ampure Xp Bead Clean:

**Prepare Ampure beads, ethanol and tubes:**
 
1. Remove beads from high DNA fridge. Allow to come fully to room temperature.
2. Label to include “PBD” in your label.
3. Prepare a 80% ethanol solution daily. Pouring 40 mL of ethanol into a 50 mL falcon tube. Add 10 mL of MGW. Invert a couple times to mix. 

**Purify your PCR1 using Ampure beads:**
 
4. Remove PCRs from fridge. Gently vortex and spin down. 
5. Determine what quantity of beads you will need. Standard Ampure for ~200 bp fragment is 1.1 bead to PCR ratio (unless super small amplicon)
6. Multiply this ratio with the amount of PCR product.
	- Multiply by the total number of samples you have and add 10% for error: 
(# of samples) x (# of µL of beads/sample) x 1.1 = total volume of beads
7. Pipette calculated volume of beads into large 1.5-5 mL tube. 
8. Carefully pipette correct volume of beads into plated PCR product.
9. Let sit at room temperature for 5 minutes. 
10. Dispose of any remaining Mag-Bind beads. 
Move open sample tubes on to magnetic plate for 2 minutes, until solution has cleared. 
11. Remove supernatant, inspect for beads and if there are none, you can discard the supernatant into the “Hazardous Waste” container.
12. Pour your freshly made 80% ethanol solution into the sterile reservoir. 
13. Add 200 µL of ethanol and let incubate for 30 seconds. Do not pipette up and down.
14. Remove supernatant with a pipette and discard.
15. Add 200 µL of ethanol to each sample and let incubate for 30 seconds.
16. Dispose of any remaining ethanol in reservoir. Add to “Hazardous Waste” container. 
17. Remove supernatant from samples with a pipette and discard.
18. Allow to sit (with lids open) for 3-5 minutes until residual ethanol is gone. 
19. During this time, monitor your beads closely. It is critical that you avoid allowing the beads to dry out while waiting for the ethanol to evaporate
20. Pour enough nuclease free dH2O into third reservoir for your elution step. 
21. Elute your DNA in water. Make sure your samples are not on the magnetic plate. Add 40 µL of Ultra Pure dH2O.
22. Seal plate and vortex. 
23. Let sit at room temperature for 5 minutes.
24. Place samples on magnetic plate for 2 minutes, until solution has cleared. 
25. Remove supernatant with a pipette, trying to avoid the beads, and transfer into clean, freshly labeled plate. It is okay if you transfer a small amount of beads with the supernatant. 
26. Close plate and spin down in mini centrifuge. Note that for every future step, you will need to place your samples on a magnetic plate. 


#### Barcoding & Indexing PCR

**Primer Sequences Used**: Illumina Nextera UDI primer sequences

| PCR Primer Name | Direction | Sequence (5’ -> 3’)|
| ----- | ----- | ----- |
| Illumina-Nextera-UDI-PCR-F Index 1 (i7) Adapters | forward | CAAGCAGAAGACGGCATACGAGAT-[**i7**]-GTCTCGTGGGCTCGG |
| Illumina-Nextera-UDI-PCR-R Index 2 (i5) Adapters| reverse | AATGATACGGCGACCACCGAGATCTACAC-[**i5**]-TCGTCGGCAGCGTC|

**Reaction Mixture**: PCR reagents, volumes, initial and final concentrations

| Reagent |Volume (μL) per plate| Volume (μL) per reaction | Initial concentration| Final concentration|
| ----- | ----- | ----- |----- |----- |
| NEB Phusion High Fidelity Master Mix |1300| 12.5 |100% |50% |
| Forward Primer |65| 0.625 |10 μM |0.25 μM |
| Reverse Primer |65| 0.625 |10 μM | 0.25 μM |
| Nuclease-Free Water |650|6.25 | N/A|N/A |
| Template DNA|N/A| 5 | 100%|20% |
| **Total**|**2392**| **25** | **N/A** |**N/A**|

This table breaks down the mixture per plate and per reaction. When running full plates (96-wells), each reagent volume was multiplied by 104 (96+8 extra sample volumes to account for pipetting error) when preparing the final master mix.

**PCR Cycling Program**: 

| PCR step | Temperature | Duration | Repetition |
| ----- | ----- | ----- | ----- |
|Initial denaturation|	95°C	|5min|	1X|
|**Normal Cycling**||||
|Denaturation|	98°C|	30s|	8X|
|Annealing|	56°C|	30s	|8X|
|Extension 	|72°C	|3min	|8X|
|Extension 	|72°C	|5min	|1x|
|Hold	|4°C	|∞	|1X|

**Step-by-Step Instructions:**

*Note: When possible, PCR set-up should be carried out in a separate pre-PCR space that is distinct from the post-PCR space where thermocyclers are located, and all post-PCR processing is performed. No equipment, consumables, or reagents should be shared between pre- and post-PCR spaces with a unidirectional flow of sample processing. This step is post-PCR and thus should occur in the post-PCR spaces.*

1. Set out Illumina Nextera UDI primers and samples to thaw.
2. Vortex and spin down thawed samples, primers, and nuclease-free water. Then tap/flick Phusion HiFi Master Mix rather than vortexing before spinning down. Thawed reagents should be stored in a cooling block or fridge when not in use.
3. Pool master mix and water reagents as denoted above in the reagent mixture table.
4. Aliquot 18 μL of master mix into each well of the PCR plate. The plate should sit in a cold block to ensure the reagents remain at a low temperature.
5. Load forward and reverse primers to respective samples following your designed plate map.
6. Add 5 μL PCR1 template to each well.
8. Seal the PCR plate with foil.
9. Spin down the plate, and then transport in a PCR cooler rack before placing it in the thermocycler.
10. Run thermocycler protocol.

**Purify your PCR2 using Ampure beads:**

Follow the protocol as described above, but using PCR2 product.

#### PCR Normalization and Pooling

1. Cleaned PCR2 product is then normalized using [SequalPrep Normalization Kit](https://documents.thermofisher.com/TFS-Assets/LSG/manuals/sequalprep_platekit_man.pdf) following the manufacturers instructions. We retained all excess product post incubation as a back up stock of PCR2 product.
2. Samples were then pooled together by adding 10 μL of each normalized sample to the pool. One plate results in 960 µL of 1 ng/µL final pool.

#### Bead Clean Concentration

We then ran the above Bead Clean concentration protocol using **0.8 bead to final library ratio** and eluting in **25 µL of Molecular grae water**.

**NOTE THAT THIS IS A DIFFERENT RATIO & ELUTION VOLUME**


#### Quality Control

Final library was quantified to verify DNA concentration using the [NOAA-PMEL-OME-Qubit-Quantification-Protocol-BeBOP](https://github.com/HanWeinrich/NOAA-PMEL-OME-Qubit-Quantification-Protocol-BeBOP/blob/main/NOAA-PMEL-OME_Qubit_Quantification_Protocol.md).

Library size selection was measured using an Agilent TapeStation [High Sensitivity Genomic DNA ScreenTape Analysis following the manufacturer's protocol](https://www.agilent.com/cs/library/usermanuals/public/HS_gDNA_QuickGuide.pdf).


#### Sequencing

Libraries were prepared for sequencing following the [16S Metagenomic Sequencing Library
PreparationPreparing 16S Ribosomal RNA Gene Amplicons for the
Illumina MiSeq System](https://support.illumina.com/documents/documentation/chemistry_documentation/16s/16s-metagenomic-library-prep-guide-15044223-b.pdf) protocol from the manufacturer. Libraries were loaded at 6pM with 20% PhiX. 

Sample library pools were sequenced on an Illumina MiSeq (San Diego, CA) at the NOAA NWFSC Conservation Biology Division using the MiSeq Reagent Kit V3 PE 2x300bp. 

### Basic troubleshooting guide

- Use built in verfification and quality control steps to confirm success of library preparation steps prior to sequencing. Built in checks include:
	- PCR1 gel visualization
	- PCR 2 gel visualization
	- Final library QuBit concentration
	- Final library size selection


## REFERENCES
- 16S Metagenomic Sequencing Library
PreparationPreparing 16S Ribosomal RNA Gene Amplicons for the Illumina MiSeq System. (2013). https://support.illumina.com/documents/documentation/chemistry_documentation/16s/16s-metagenomic-library-prep-guide-15044223-b.pdf
- Curd EE, Gold Z, Kandlikar GS, et al. Anacapa Toolkit: An environmental DNA toolkit for processing multilocus metabarcode datasets. Methods Ecol Evol. 2019; 10: 1469–1475. https://doi.org/10.1111/2041-210X.13214
- Gold, Zachary, Emily E. Curd, Kelly D. Goodwin, Emma S. Choi, Benjamin W. Frable, Andrew R. Thompson, Harold J. Walker Jr et al. "Improving metabarcoding taxonomic assignment: A case study of fishes in a large marine ecosystem." Molecular ecology resources 21, no. 7 (2021): 2546-2564.
- Gold, Zachary, Adam R. Wall, Teia M. Schweizer, N. Dean Pentcheff, Emily E. Curd, Paul H. Barber, Rachel S. Meyer et al. "A manager’s guide to using eDNA metabarcoding in marine ecosystems." PeerJ 10 (2022): e14071.