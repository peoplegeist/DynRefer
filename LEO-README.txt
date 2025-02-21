install
=======
do not run setup.sh

pip install --upgrade pip

pip install torch==2.2.1 torchvision==0.17.1 --index-url https://download.pytorch.org/whl/cu121
pip install scikit-learn==1.3.2

pip install -r requirements.txt (based on ticket https://github.com/callsys/DynRefer/issues/9)
-- removed the nvidia drivers and transformers==4.28.0

python -m spacy download en

pip install salesforce-lavis==1.0.2

install for demo-app
=====================
pip install gradio (ignore dependecy warnings)
pip install demo/segment_anything/



data & model
============



run
==============
python  ./demo/dynrefer_inference.py

changelog
==========
#- float16 instead of bfloat # will cause caption to come out as 'ssss', needs GPU with bfloat16 support.
- added ./ to sys python path in app.py and dynrefer_inference.python
- adjust demo_dynrefer.yaml: "load_ckpt_path: "ckpts/refcocog_ft.pth"
