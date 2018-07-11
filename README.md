# HaarCascade_facedetection
# Training my own haarcascade file
    mkdir data 
    mkdir info
    1.opencv_createsamples -img typeimagename.jpg -bg bg.txt -info info/info.txt -pngoutput info -maxxangle 0.5 -maxyangle 0.5      -   maxzangle 0.5 -num 1900 
    The numimages should be less than the negative image count(Eg if negative image is 1950 use 1900)
     2.opencv_createsamples -info info/info.txt -num 1900 -vec positives.vec 
    To create positive vector files
     3.opencv_traincascade -data data -vec positives.vec -bg bg.txt -numPos 1800 -numNeg 900 -numstages 12
    Here the positive must higher and negatives must be half
