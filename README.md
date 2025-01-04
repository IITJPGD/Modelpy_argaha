


```
python -m venv venv

or python3 -m venv venv


On Windows:

.\venv\Scripts\activate
On macOS/Linux:

source venv/bin/activate



pip install -r requirements.txt



python main.py --root /Users/jojojoseph/Documents/IITJ/Modelpy_argaha/data/FoETrainingSets180/ --g-model g_tnrd --d-model d_tnrd --model-config "{'gen_blocks':3, 'dis_blocks':4, 'in_channels':1}" --reconstruction-weight 1.0 --perceptual-weight 0 --adversarial-weight 0 --tnrd-energy-weight 0 --crop-size 100 --gray-scale --noise-sigma 50 --epochs 600 --step-size 150 --batch-size 2 --eval-every 10 --print-every 100 --lr 1e-3


```


Deactivate the virtual environment
```
deactivate
```



Notes for Colab 
Change the run time type to T4 GPU in Google Colab)

1.⁠ ⁠Upload the “denoising” folder to the Google drive and then to the Colab run time as discussed. (make sure the name of the folder is always “denoising”, if not rename it to it, as the name is involved in path names in few code files)

2.  Enter the following command in Colab to get a command shell

!pip
 install google-colab-shell

from google_colab_shell 
import getshell

getshell()



3.⁠ ⁠Then type “ pip install tensorboardX ” in the shell.

4.⁠ ⁠Then enter “ cd denoising ”.

5.⁠ ⁠Now eneter the running command:

python main.py --root /content/denoising/data/FoETrainingSets180/ --g-model g_tnrd --d-model d_tnrd --model-config "{'gen_blocks':3, 'dis_blocks':4, 'in_channels':1}" --reconstruction-weight 1.0 --perceptual-weight 0 --adversarial-weight 0 --tnrd-energy-weight 0 --crop-size 100 --gray-scale --noise-sigma 50 --epochs 600 --step-size 150 --batch-size 2 --eval-every 10 --print-every 100 --lr 1e-3