Data paper
================

### F. Ehtemam<sup>1+</sup>, H. Wang<sup>2+</sup> and A. van den Bogert<sup>2</sup>

<sup>1</sup> University of Maryland & <sup>2</sup> Cleveland State University

<sup>+</sup> F. Ehtemam and H. Wang have contributed equally to this work.
Copyright © 2017 Cleveland State University

------------------------------------------------------------------------

The most important question before discussing anything is that if publishing a data paper will prevent us from publishing future analysis based on the data or not. This page lists publishers that do not have any problem with the data being published earlier:
<https://f1000research.com/data-policies>
It is quite a large list so I think we can have the dataset published.

General considerations
----------------------

### Article name

Suggestions for the name of the article:
1. "Kinematics and kinetics of normal and perturbed walking on the treadmill: a comprehensive gait dataset" or variants of this
2.
3.

### Where to publish

#### Peer-reviewed (data journals)

Some major data journals:

-   Scientific Data
    -   Publisher: Nature
    -   Fee: $1350
    -   Data hosting: Up to 100 GB free at figshare
    -   Link: <https://www.nature.com/sdata/publish/submission-guidelines>
-   GigaScience Data Notes
    -   Publisher: Oxford Academic
    -   Fee: $1015
    -   Data hosting: Up to 1 TB free at their GigaDB repository
    -   Link: <https://academic.oup.com/gigascience/pages/data_note>
-   Data in Brief
    -   Publisher: Elsevier
    -   Fee: $500
    -   Data hosting: Not available
    -   Link: <https://www.elsevier.com/journals/data-in-brief/2352-3409/guide-for-authors>

#### Peer-reviewed (general)

There are journals that are not specifically targeted towards publishing data papers but they will accept data papers as well (e.g. PeerJ). However, these journals are open access too and they charge similar publication fees as data journals mentioned above.

#### Non peer-reviewed

Alternatively one can publish their article on many repositories available online and host the data in a separate repository. The advantage is that this will be free but the authors don't get any feedback on their methods and data practices.
Some of the famous online repositories for publication:

-   <https://arxiv.org/>
-   <https://www.biorxiv.org/>
-   <https://osf.io/preprints/>
-   <https://peerj.com/preprints-search/>
-   <https://f1000research.com/>

### Funding options

UMD funds 50% of the cost for open access publishing (<https://www.lib.umd.edu/oa/openaccessfund>). I don't know if a similar thing is available at CSU or not. Most universities these days have funds to support open access publishing. It could be through their libraries or a separate office. It doesn't hurt to ask if CSU has this.

Statement of significance
-------------------------

An important part of any publication is to show its contribution to what is already available. Without a significant contribution there is no publication. The publication of this dataset has three major and six minor (arguably) contributions:

Major:

-   Availability of EMG data
-   Availability of accelerations
-   Availability of processed data

Minor:

-   Providing the data in the format readable by OpenSim
-   Providing the 2D joint moments
-   The data provides responses to two different amplitudes of perturbation.
-   The data provides responses to two different types of mechanical perturbations (AP vs. ML).
-   It provides data for more subjects than previous datasets.
-   It provides more data per subject per condition compared to any other dataset (we have 16 minutes of walking for each amplitude of perturbation while PeerJ data had 8 minutes).

Data organization
-----------------

### Raw data <a name="Raw data"></a>

It is extremely important to publish the raw data. Any processed data has followed a certain method of processing that can make future applications limited or impossible due to the fact that different research questions require different methods of processing. So researchers must have access to the raw data. However, raw data does not necessarily mean unstructured data. Even the raw data has to be structured in a way that makes it easy for the user to understand and access different types of data within the dataset. So I think the following raw data have to be written in separate files and labeled appropriately:

-   Kinematics
-   GRFs
-   EMGs
-   Accelerations
-   Treadmill files (speeds and accelerations)
-   Designed perturbations

In addition to this I suggest an organization that separates normal walking and antero-posterior and medio-lateral perturbations. Furthermore, the data can be uploaded in two sets: a set called 21 subjects and a set called 15 subjects. While the 15 subjects were the same as the ones in 21 subjects set, these 15 are the ones for which EMGs and accelerations are available. This separation makes it easier for people with certain research questions to access the data.

### Processed data

As important as publishing the raw data is, so is providing some sort of processed data. Biomechanics is an interdisciplinary field with people from very different backgrounds. Not everyone is tech-savvy enough to program scripts that allows them to analyze the raw data. What type of processed data one publishes depends on the field of study.
It is common for studies in biomechanics to look at time normalized gait data. In addition to research questions that use this type of data in their investigations, this can be a highly useful educational resource. I was always disappointed by the lack of a simple dataset from couple of subjects that I could use to practice the knowledge I got from biomechanics courses through exploring different analysis methods using the data. We are going to change this by publishing the following time normalized data:

-   Marker data
-   Joint angles
-   GRFs
-   EMG
-   Accelerations
-   2D joint moments (sagittal plane)

We will also include the graphs showing averages of processed data across all cycles to make it easy for people to compare it to what they already know from literature. In addition, we will provide the scripts we used to process the data. This includes a reference to Jason's GaitAnalysisToolkit we used for gap filling kinematics and the codes from Sandy and Huawei on inertial compensation.

Agenda
------

Here is a list of steps (some of them already done) in order to prepare the raw and processed datasets before the manuscript is written:

-   Structure the raw data according to the suggestion from above (see [Raw data](#Raw%20data))
-   Fill all the gaps in kinematics using Jason's package (done in the spring)
-   Do the belt speed compensation and pitch sway compensation on GRFs (done by Huawei)
-   Calculate 2D joint moments using leg2d code. (done by Huawei)
-   Have all steps of processing replicated at Maryland and Cleveland to make sure we get the same processed data. (in progress)
-   Time normalize the data and write it to appropriate formats (both CSV and OpenSim formats)
-   Prepare graphs of averaged values across all cycles
-   Write a codebook that explains the data structure and the file formats and has to be uploaded with the dataset. (Has been done but the current version has to be expanded with some more details)
