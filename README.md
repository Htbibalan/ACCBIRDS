
**🏗️ 🚧⚠️🚧 This repository is under construction 🚧⚠️🚧🏗️**
# BAT : Behavioural Annotator Tool 🦇
 
![Banner Image](https://github.com/Htbibalan/BAT/blob/main/src/banner_2.png)

**BAT** is a Python-based graphical tool designed to help researchers annotate animal behaviour from video recordings and synchronize these annotations with external devices with timestamped data.
Here, we are focused on accelerometer (ACC) data collected from devices mounted on the back of birds, but BAT can be generalized for other experimental settings.

### Current development focus (April 2026):  📝
**For now, I am trying to establish a reliable behavioural annotation GUI, to timestamp behaviours of birds and save .csv files with labeled ethograms. ( duration, number and timestamp of events)**

**I am thinking of multi-observer / multi-animal support + gamepad integration to make long annotation sessions faster and less tiring by gamifying the process. This would also help with generating reliable ground truth by parallel scoring of behaviours or reducing the workload of each user, such that each user ( I call them players) focus on particular behaviours and score the same video**

**Need to work on tracking of multi-animals and annotation of each in parallel**


### Highlights ✅
- Frame-accurate video playback & navigation
- Bout mode (start–end) and Event mode (instant markers)
- Custom ethogram (user-defined behaviour list)
- Optional absolute start datetime → real ISO timestamps
- Undo / delete / clear annotations
- Treeview preview + CSV export (includes fps, video name, input datetime…)
- Multi-observer / multi-animal mode : assign annotations to different players & animals
- Gamepad support (via pygame) : map buttons & keys per player
- Parallel or exclusive bout policy
- Visual HUD showing active bouts during playback
- Sound feedback & overlay messages




## How to run it? 🎚️

#### Advanced development mode
#### 1. Clone the repository

```bash
git clone https://github.com/Htbibalan/BAT.git
cd BAT
```

#### 2. Install the anaconda env
**use the environment.yml file located in ACCBIRDS/src to install the env using the command below**

                  conda env create -f environment.yml

#### 3. Run the tool
**Switch to the env named BAT using:**
                
                    conda activate BAT
                    python BAT.py

#### Easy installation
Download the latest release (Windows installer):
https://github.com/Htbibalan/BAT/releases/latest
and install the software.


## Gamepad & Multi-observer mode 🎮🐦‍⬛🐦🎮

Goal: allow multiple people  to annotate efficiently. Multiple players can score/annotate a single animal, or each annotate a different animal in the same video.
##### Default controls (in progress 🚧)

| Action                     | Keyboard              | Gamepad (common)           |
|----------------------------|-----------------------|----------------------------|
| Play / Pause               | Space / Enter         | Start button (~#7)         |
| Frame -1 / +1              | ← / →                 | D-pad left / right         |
| Frame -100 / +100          | ↑ / ↓                 | D-pad up / down            |
| Continuous seek            | —                     | Left stick X-axis          |
| Undo last annotation       | —                     | Back / Select (~#6)        |
| Trigger behaviour          | Custom per player     | Custom buttons per player  |

Use the **Inputs** tab to remap buttons/keys for each player.



#### Acknowledgments 📢

* Supported by ([BiRBSLAB](https://btomotani.wordpress.com/)), UiT The Arctic University of Norway.
* User-experience feedback by Fernando Ramón García Fernández , Radboud University Nijmegen

## Citation
Taghipourbibalan, H., García Fernández, F. R., & Tomotani, B. M. (2026). 
BAT: Behavioural Annotator Tool (Version 1.0.0) [Software]. Zenodo. 
https://doi.org/10.5281/zenodo.19855759




### To do 🛠️
* fix keyboard shortcuts ( backspace, undo)
* add HUD hide option
* add experiment/ user/ folder structure 
* add project load/save feature
~~overkill: include animal labeling for multi-animal annotations ( e.g. simple computer vision to mark/tag the animals, ideally this should be done in advance by the user)~~
* add multiple window expansion for multi-user in parallel scoring