
**🏗️ 🚧⚠️🚧 This repository is under construction 🚧⚠️🚧🏗️**
# BAT : Behavioural Annotator Tool 🦇
 
![Banner Image](https://github.com/Htbibalan/BAT/blob/main/src/banner.png)

**BAT** is a Python-based graphical tool designed to help researchers annotate animal behaviour from video recordings and synchronize these annotations with external devices with timestamped data.
Here, we are focused on accelerometer (ACC) data collected from devices mounted on the back of birds, but BAT can be generalized for other experimental settings.

### Current development focus (February 2026):  📝
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
- Chunked reading for very large accelerometer files



## Quick Start 🎚️

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
In Jupyter Notebook or your preferred IDE, run one of the notebooks in the /notebooks folder.
bat_v02.2.ipynb is the simplest one and should work for now, there you can load videos, define ethograms, and start annotating, it is recommended to enter the time/data of the video in the field to have proper time stamp of the behaviours for further synchronization with external devices/data sets.


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
* User-experience feedback by Fernando Fernández 




### To do 🛠️
* fix keyboard shortcuts ( backspace, undo)
* add HUD hide option
* add experiment/ user/ folder structure 
* overkill: include animal labeling for multi-animal annotations ( e.g. simple computer vision to mark/tag the animals, ideally this should be done in advance by the user)