Read me
=======================================================

Every dataset is publicly available via the GigaDB repository. This manual describes data usage. 
The details of data set description, converted data, raw data, sample code, and sample
data are described below. You can check contents by referring to the
list. The subjects (S1-S25, aged 20-34 years, 15 males and 10 females)
were asked to perform 11 different movement tasks: arm-reaching for six
multi-direction, hand-grasping for three objects, and wrist-twisting
with two different motions.

=======================================================
**Contents**

I.  Data set description
II.  Converted data
III.  Raw data
IV.  SampleCode
V.  SampleData
=======================================================
****
=======================================================
### I. Data set description

  -   The data set is acquired by cue information. Each session has cues
      as trigger information.
  -   Channel labels show position of each electrode: EEG electrodes (1-31
      and 36-64), EOG electrodes (32-35), and EMG electrodes (65-71)

  1.  **Trigger information**

    1-1. Arm reaching

        class       Forward   Backward    Left    Right    Up    Down   Rest
  --------------  ---------   ----------  ------  -------  ------  ------  ------
   trigger code     S 11        S 21      S 31    S 41    S 51   S 61     S 8

    1-2. Hand grasping

        class         Cup    Ball    Card   Rest
  --------------   ------  ------  ------  ------
   trigger code    S 11   S 21   S 61    S 8

    1-3. Wrist twisting

        class       Pronation    Supination     Rest
  --------------  -----------   ------------   ------
   trigger code     S 91          S101          S 8

    1-4. Start and end of experiment

        class        Start    End
  --------------  -------  ------
   trigger code   S 13    S 14

  2.  **Channel labels**

   channel    label   channel   label   channel   label    channel     label    channel     label
  ---------  -------  --------- ------- --------- --------  ---------   -------  ---------  ----------
      1         Fp1       16        C3       31       POz        46         FT8       61          O1
      2         AF7       17        C1       32      EOG_1      47         C2        62          Oz
      3         AF3       18        Cz       33      EOG_2      48         C4        63          O2
      4         AFz       19        TP7      34      EOG_3      49         C6        64          Iz
      5          F7        20       CP5      35      EOG_4      50         T8        65        EMG_1
      6          F5        21       CP3      36       Fp2        51         CP2       66       EMG_2
      7          F3        22       CP1      37       AF4        52         CP4       67       EMG_3
      8          F1        23       CPz      38       AF8        53         CP6       68       EMG_4
      9          Fz        24        P7       39        F2        54         TP8        69       EMG_5
     10        FT7       25        P5        40        F4        55         P2         70       EMG_6
     11        FC5       26        P3        41        F6        56         P4         71       EMG_Ref
     12        FC3       27        P1        42        F8        57         P6              
     13        FC1       28        Pz        43       FC2       58          P8              
     14         T7        29       PO7      44       FC4       59         PO4             
     15         C5        30       PO3      45       FC6       60         PO8             
=======================================================

=======================================================
### II. Converted data

  -   If you want to download data of .mat file, you can download it from
      `Converted data'.

  1.  **Download data from the GigaDB repository**

    1-1. Go to the GigaDB repository       

    1-2. Select the file you want and click the download button at the top
    to download it.

  2.  **Description of each file**

    2-1. Subject 

    Uploaded data as subject number        
    ex) sub1, sub2, ..., sub25

    2-2. Recording

    Each folder of converted data contains corresponding data to EEG, EMG, and EOG signals 

      -   2_EEG_ConvertedData
      -   3_EMG_ConvertedData
      -   4_EOG_ConvertedData

    2-3. Files for each class

    The files contains arm-reaching, hand-grasping, and wrist-twisting signals' data, and data
    types are real movement and motor imagery separately.

      -   Class name

      Reaching, multigrasp, and twist

      -   Paradigm

      MI : Motor imagery
      realMove: Real movement

  Name              Description
  ---------------   --------------------------------------------------
  dat.x                Pre-processed data
  dat.fs               Sampling frequency
  dat.file             File name
  dat.clab            Channel information
  mnt.x               X coordinates for channel position
  mnt.y               Y coordinates for channel position
  mnt.pos_3d       3D coordinates for channel position
  mnt.clab           Channel information
  mrk.pos            Trigger marking time
  mrk.toe            Trigger number
  mrk.fs              Sampling frequency
  mrk.y               Class lables
  mrk.className   Class name
  mrk.mics           Starting and end point information of experiment

### 
=======================================================

=======================================================
### III. Raw data

  -   If you want to download data of raw file, you can download it from `Raw data'.

  1.  **Download data from the GigaDB repository**

    1-1. Go to the GigaDB repository. 

    1-2. Select the folder you want and click the download button at the
    top to download it.

  2.  Description of each file

    2-1. Subject 
    
    Uploaded data as subject number
    ex) sub1, sub2, ..., sub25

    2-2. Recording

    1_RawData folder contains entire data from 25 subjects recorded over three sessions

    2-3. Files for each class

    The files are about reaching, grasp and twist, and they are about
    executed movement and imagination movement, respectively.

      -   Class name

      Reaching, multigrasp, and twist

      -   Paradigm

      MI : Motor imagery
      realMove: Movement execution

  Name                           Description
  ---------------------         --------------------
  session1_sub1_XXX.eeg       Raw signals
  session1_sub1_XXX.vhdr      Header information
  session1_sub1_XXX.vmrk     Marker information

### 
=======================================================

=======================================================
### IV. SampleCode

  -   If you want to run sample code, you can download the each . m file
      in `5_Scripts' folder

  1.  **Download data from the GigaDB repository**

    1-1.  Go to the GigaDB repository.

    1-2. Download bbci_toolbox.zip in `Reference_toolbox' folder

    1-3. Unzip the downloaded bbci_toolbox.zip

    1-4. Download every .mat files in `5_Scripts' folder

  2.  Description of each folder

      -   Each mat file has a detailed comments

    2-1. Data_Analysis.m

  This is about the functions for sample code execution. This file
  contains execution codes for sample codes.

      -   Convert: Data_Convert.m
      -   Performance measurement: ACC_ArmReaching, ACC_HandGrasping, ACC_WristTwisting
      -   Converting_Arrow: It contains trigger information for converting raw files

    2-2. Visualization.m

    This is about the functions for sample code execution. This file
    contains execution codes for sample codes and the instruction to run EEGLAB for event-related spectral perturbation analysis.

### 
=======================================================

=======================================================
### V. Sample_Data

    -   To execute sample codes, please download the SampleData beforehand. 
    -   The sample data is provided as an example. To apply another subject,
        download extra data files following above two contents, raw data and
        converted data.

=======================================================