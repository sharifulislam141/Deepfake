#Clone <br>
git clone https://github.com/sharifulislam141/Deepfake<br>
cd roop<br>
pip install -r requirements.txt<br>

#download model <br>
pip uninstall onnxruntime onnxruntime-gpu -y<br>
pip install torch torchvision torchaudio --force-reinstall --index-url https://download.pytorch.org/whl/cu118<br>
pip install onnxruntime-gpu<br>


#use<br>

python run.py --target /content/bryan.mp4  --source /content/tom.jpg -o /content/swapped.mp4 --execution-provider cuda --frame-processor face_swapper face_enhancer
