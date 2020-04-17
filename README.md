# Face-Liveness
**Note: Install important libraries and dependencies from the link mentioned below.**  
1.Create two videos,one should have real faces(save it with the name real) and the other one should only contain a video playing in a phone(fake).
{Remember:-both videos must be of same person)


2.Run command for fake video:
python gather_examples.py --input videos/fake.mp4 --output dataset/fake \
	--detector face_detector --skip 1


3.Run command for real video:
python gather_examples.py --input videos/real.mp4 --output dataset/real \
	--detector face_detector --skip 4


4.Train the model:
python train.py --dataset dataset --model liveness.model --le le.pickle



5.python liveness_demo.py --model liveness.model --le le.pickle \
	--detector face_detector
# Credits:
https://www.pyimagesearch.com/2019/03/11/liveness-detection-with-opencv/

# Proper Documentation Coming Soon...
