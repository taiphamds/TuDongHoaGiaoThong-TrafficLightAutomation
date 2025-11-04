# Traffic Light Control using YOLO – Personal Project
At traffic light intersections, when traffic density is high, the default light duration is around 60 seconds — this balances between clearing the main flow and not delaying the opposite direction too long.
However, when traffic density is light — imagine there’s only one person waiting at a red light and the minimum red time is still about 20 seconds — this becomes inefficient. To optimize, I propose an algorithm that skips unnecessary red time and instead calculates the green light duration based on the average number and type of waiting vehicles (e.g., motorbike: 3s, car: 4s, truck/bus: 5s) from the two opposite lanes currently waiting at the red light.

## Example:
At a four-way intersection (East–West–South–North; East–West are opposite, South–North are opposite), the light cycle is green → yellow → red. 
When the North–South green light ends and turns yellow, the camera on the East–West lane detects and counts the number of waiting vehicles and calculates the green time based on the average vehicle type. When the East–West green light ends and turns yellow, the camera on the North–South lane does the same — and the cycle continues.

## Result
https://github.com/user-attachments/assets/27f1015f-ccdf-4a90-bac0-8d0e1844684c

## Yolov8 
By Huy Ngo https://www.kaggle.com/code/vhn1305/traffic-detection/output?select=yolov8n.pt
