
#include <opencv2/core/core.hpp>
#include <opencv2/highgui/highgui.hpp>
#include <iostream>
#include <opencv2/imgproc/imgproc.hpp>
using namespace cv;
using namespace std;

int main(int argc, char** argv)
{
	Mat house = imread("c:\\images\\house.jpg", CV_LOAD_IMAGE_COLOR);
	Mat yzu = imread("c:\\images\\yzu.jpg", CV_LOAD_IMAGE_COLOR);
	Mat max;
	max = 0.9 * house + 0.1 * yzu;
	imshow("123", max);

	waitKey(0);

	return 0;
}
