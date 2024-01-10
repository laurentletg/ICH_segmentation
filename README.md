# SEGMENTER_V2
* 3D Slicer extension
* Manual medical image segmentation 

### Installation steps
1. Install [3D Slicer](https://download.slicer.org).  
2. Clone this repository.
3. Modify `label_config.yml` to describe your annotations. There can be as many or as few as you would like. The colors are configurable using RGB integer values between 0 and 255. The default HU thresholds for each label are also configurable. These can also be modified directly in the extension. Note that additional tools will appear in the user interface if one of the labels is either intracerebral hemorrhage (ICH) or perihematomal edema (PHE). 
4. Open 3D Slicer. 
5. Activate the checkbox `Enable developer mode` in `Edit -> Application Settings -> Developer -> Enable developer mode`. 
6. Add the path of this repository in `Edit -> Application Settings -> Modules -> Additional module paths`. 
    * There might be errors. These would be seen in the Python Console. 
7. The module can be found under `Examples -> SEGMENTER_V2`. 

### Trouble shooting 
* Qt might need to be installed. The first five steps of the following procedure might be useful for this: [procedure](https://web.stanford.edu/dept/cs_edu/resources/qt/install-mac). 
* If some modules are missing (`ModuleNotFoundError`), they must be added to the 3D Slicer environment by using the following commands in the Python Console: 
        `from slicer.util import pip_install`
        `pip_install("XYZ")` where `XYZ` is replaced by the proper library

### Other extensions that could be useful
* `SlicerJupyter` to be able to use Jupyter Notebooks connected to 3D Slicer. 

### Video tutorials
The videos are much less blurry if the mp4 files are downloaded to your computer. 

[Videos](https://drive.google.com/drive/folders/1GQJi9Qqy5FyzHR690quK81nSt4WMXBbd)

### Other resources
* [3D Slicer Tutorials](https://www.youtube.com/watch?v=QTEti9aY0vs&)
* [3D Slicer Documentation](https://www.slicer.org/wiki/Documentation/Nightly/Training)