#Clone
git clone https://github.com/sharifulislam141/Deepfake
cd roop
pip install -r requirements.txt

#download model
pip uninstall onnxruntime onnxruntime-gpu -y
pip install torch torchvision torchaudio --force-reinstall --index-url https://download.pytorch.org/whl/cu118
pip install onnxruntime-gpu


#use

python run.py --target /content/bryan.mp4  --source /content/tom.jpg -o /content/swapped.mp4 --execution-provider cuda --frame-processor face_swapper face_enhancer
