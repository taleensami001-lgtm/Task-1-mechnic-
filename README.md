
# Making a preliminary design of a dog robot تصميم أولي لكلب روبوت



### **1 / disign how it looks and the structure looks اولا / تصميم شكل الجسم والهيكل**

- first i used ( paper + pencil ) for initial sketches


![img alt](https://github.com/taleensami001-lgtm/Task-1-mechnic-/blob/dc20a6d5ee323f8e27589eb816b58d3f289de4d5/IMG_6008.jpeg) 


- Then used ( Tinkercad ) to simulate my initial sketch


![imp alt](https://github.com/taleensami001-lgtm/Task-1-mechnic-/blob/718d15720152bd0e90007231c5fd232813e88f5f/IMG_1821.jpeg)

### **2 / disign the legs and it's movement  ثانيا / تصميم الأرجل وحركتها**


- Moving Forward: The robot moves the legs on the same side of its body at the exact same time.
The robot lifts and swings the Front-Right and Hind-Right legs forward together, while balancing entirely on its left side.
Once they land, it lifts and swings the Front-Left and Hind-Left legs forward.

- Moving Backward: The exact same pairing is used, but the motor directions are reversed. The robot lifts the same-side legs and swings them backward, pulling the body along.


- الحركة للأمام: الروبوت يرفع ويحرك الرجلين اللتين على نفس الجانب معاً.
يرفع (الأمامية اليمنى + الخلفية اليمنى) ويقذفهما للأمام، بينما يرتكز بالكامل على الجانب الأيسر.
في الخطوة التالية، يعكس العملية: يرفع (الأمامية اليسرى + الخلفية اليسرى) ويقدمهما للأمام.

- الحركة للخلف: يتم عكس اتجاه حركة الموتورات فقط. الأرجل ترتفع وتتحرك إلى الخلف بنفس التزامن الجانبي، مما يسحب جسم الروبوت للوراء.


![img alt](https://github.com/taleensami001-lgtm/Dog-robot/blob/36c6c952e3133bb53401d2c8f0a22a2c04b33aa0/IMG_1827.jpeg)


- Front Legs: The "knee" joints bend backward (toward the tail).
- Hind Legs: The "knee" joints bend forward (with the knees pointing toward the head).
- الأرجل الأمامية: تنحني المفاصل (الركبة) إلى الخلف.
- الأرجل الخلفية: تنحني المفاصل إلى الأمام.

![img alt](https://github.com/taleensami001-lgtm/Dog-robot/blob/1451e1dd75e799fe8472d960a482e7eb0d847dd0/IMG_1829.jpeg)


### **3 / Robot's joints & Degrees of freedom (Dof) ثالثا / عدد المفاصل ودرجات الحرية**

- 4 Joints
- 4 Dof

### **4 / Motors رابعا / المحركات**

- For the leg movement of a quadruped robot, traditional small servo motors or standard DC motors are not used, because the robot's legs are subjected to continuous impacts with the ground, requiring immense torque and an extremely fast response.
  
- لحركة أرجل كلب الروبوت (Quadruped Robot)، لا يتم استخدام محركات السيرفو التقليدية الصغيرة أو محركات الDC العادية، لأن أرجل الروبوت تتعرض لصدمات مستمرة مع الأرض وتحتاج إلى عزم دوران هائل واستجابة سريعة جداً.


### **5 / Initial torque of a joint خامسا / العزم المبدئي لأحد المفاصل**


- Torque Calculation for a 3D-Printed Plastic Component
1. Determining Torque
To calculate the torque (t), we must first determine the applied force (F) and the perpendicular distance (d) from the axis of rotation (the pivot). The formula for torque is:

 **t = Fd**

2. Calculating Force
The applied force (in this case, weight) is the product of the object's mass (m) and the acceleration due to gravity (g).

 **F = mg**

3. Calculating Volume
To find the mass, we must first calculate the volume (V) of the object. The volume of a rectangular prism is calculated by multiplying its length, width, and height: 

 **V = lengh X width X height**
 
 - and that is my Robot's length , width and height in : 

![img alt](https://github.com/taleensami001-lgtm/Dog-robot/blob/2e326a0cf153084ae895d28993d6b05be3f497ac/IMG_6012.jpeg)

 **V = 9 x 5 x 8 = 360 cm^3**

4. Calculating Mass
Mass is obtained by multiplying the volume by the density (p) of the material used. The material chosen is a 3D-printing plastic filament (e.g., PLA), known for its excellent printability, with a density of 1.21g/cm^3.

**m = Vp**
**m = 360 cm^3 X 1.21 g/cm^3 = 435.6 g**

5. Unit Conversion
To strictly adhere to standard SI physics units (calculating Force in Newtons), the mass must be converted from grams to kilograms by multiplying by 10^-3 (or dividing by 1,000):

**m = 435,6 X 10^-3 = 0.4356 kg**

6. Final Force and Torque Calculation
Now, we multiply the mass in kilograms by the standard gravitational acceleration (g = 9.8m/s^2):

**F = 0.4356 kg X 9.8 m/s^2 = 4.27 N**

7. Finally, to find the torque, substitute this force back into the initial torque equation and multiply it by the given distance from the axis of rotation:

**t = Fd**
**t = 4.27 N X 2 = 85.4 Nm**