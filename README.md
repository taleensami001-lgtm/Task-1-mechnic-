
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

- حساب العزم لقطعة بلاستيكية مطبوعة بتقنية ثلاثية الأبعاد
1. تحديد العزم
لحساب العزم، يجب أولاً تحديد القوة المؤثرة والمسافة العمودية من محور الدوران (نقطة الارتكاز). صيغة حساب العزم هي:
 
**العزم = القوة × المسافة.**

2. حساب القوة
القوة المؤثرة (وفي هذه الحالة هي الوزن) ناتجة عن حاصل ضرب كتلة الجسم في عجلة الجاذبية الأرضية. الصيغة هي: 

**القوة = الكتلة × الجاذبية.**

3. حساب الحجم
لإيجاد الكتلة، يجب أولاً حساب حجم الجسم. يُحسب حجم المنشور المستطيل بضرب الطول في العرض في الارتفاع، الصيغة هي: 

**الحجم = الطول × العرض × الارتفاع.**
**الحجم = 9 × 5 × 8 = 360 سم مكعب.**

4. حساب الكتلة 
يتم الحصول على الكتلة بضرب الحجم في كثافة المادة المستخدمة. المادة المختارة هي خيوط البلاستيك المخصصة للطباعة ثلاثية الأبعاد (مثل مادة PLA)، والمعروفة بقابليتها الممتازة للطباعة، وتبلغ كثافتها 1.21 جرام/سم مكعب.
الصيغة هي: 

**الكتلة = الحجم × الكثافة.**
**الكتلة = 360 سم مكعب × 1.21 جرام/سم مكعب = 435.6 جرام.**

5. تحويل الوحدات
للالتزام الصارم بوحدات النظام الدولي القياسية في الفيزياء وحساب القوة بوحدة النيوتن، يجب تحويل الكتلة من الجرام إلى الكيلوجرام عن طريق الضرب في 0.001 (أو القسمة على 1,000):

**الكتلة = 435.6 × 0.001 = 0.4356 كيلوجرام.**

6. الحساب النهائي للقوة والعزم
الآن، نضرب الكتلة بالكيلوجرام في عجلة الجاذبية الأرضية القياسية (9.8 متر/ثانية مربعة):

**القوة = 0.4356 كيلوجرام × 9.8 متر/ثانية مربعة = 4.27 نيوتن.**

7. وأخيرًا، لإيجاد العزم، نعوض بقيمة هذه القوة في معادلة العزم الأولية ونضربها في المسافة المحددة من محور الدوران:

**العزم = القوة × المسافة.**
**العزم = 4.27 نيوتن × 2 متر = 8.54 نيوتن.متر.**


### **6 / Stability and the Center of Gravity of the robot سادسا / الثبات ومركز الجاذبيه لدى الروبوت**


- Center of Gravity (CoG)

• Theoretical Location: In a rectangular body with uniform mass distribution, the Center of Gravity is located exactly at the geometric center (the intersection of the diagonals in the middle of the chassis).
• Actual Location: This center shifts depending on the placement of heavy components. For example, heavy motors (such as high-torque BLDC motors typically used in the leg joints) and batteries will pull the CoG towards them.
• Rule of Thumb: The lower the CoG (closer to the ground) and the more centered it is within the chassis, the greater the robot's resistance to tipping over or losing balance.


- Stability 
The stability of the robot depends on a geometric and physical principle known as the Support Polygon. This is the 2D ground area formed by drawing imaginary lines connecting the contact points of the robot's feet with the ground.
Based on the robot's movement, stability is divided into two main types:
• Static Stability: When the robot stands on all four legs, the support polygon forms a rectangle. The robot is completely stable as long as the vertical projection of its CoG falls within the boundaries of this rectangle. If the robot lifts one leg to walk slowly, the support polygon turns into a triangle; to avoid falling, the robot's movement must be programmed so that its body leans slightly, shifting the CoG inside this new triangle before lifting the leg.
• Dynamic Stability: When the robot dog moves faster, such as in a trotting gait (Trot), it lifts two diagonally opposite legs at the same time. In this case, the support polygon shrinks to a mere diagonal straight line. Here, the robot temporarily loses its static stability and relies on its continuous kinetic balance and forward momentum to avoid falling, rapidly switching the legs in contact with the ground before it loses balance.


- مركز الجاذبية (Center of Gravity - CoG)
• الموقع النظري: في الجسم المستطيل ذي التوزيع المتساوي للكتلة، يقع مركز الجاذبية في المركز الهندسي تماماً (نقطة تقاطع الأقطار في منتصف الهيكل).
• الموقع الفعلي: يتغير هذا المركز استجابةً لأماكن تمركز الأجزاء الثقيلة. على سبيل المثال، المحركات الثقيلة (مثل محركات BLDC ذات عزم الدوران العالي المستخدمة عادةً في مفاصل الأرجل) والبطاريات ستسحب مركز الجاذبية نحوها.
• القاعدة الأساسية: كلما كان مركز الجاذبية منخفضاً (أقرب للأرض) ومتمركزاً في منتصف الهيكل، زادت مقاومة الروبوت للانقلاب أو فقدان التوازن.


- الثبات (Stability)
يعتمد ثبات الروبوت على مبدأ هندسي وفيزيائي يُعرف باسم مضلع الدعم، وهو المساحة الأرضية التي تتشكل عند رسم خطوط وهمية تصل بين نقاط تلامس أقدام الروبوت مع الأرض.
ينقسم الثبات بناءً على حركة الروبوت إلى نوعين أساسيين:
• الثبات الساكن (Static Stability): عندما يقف الروبوت على أرجله الأربعة، يشكل مضلع الدعم مستطيلاً. يكون الروبوت مستقراً تماماً طالما أن الإسقاط العمودي لمركز جاذبيته يسقط داخل حدود هذا المستطيل. وإذا رفع الروبوت رجلاً واحدة للمشي ببطء، يتحول مضلع الدعم إلى مثلث؛ ولتجنب السقوط، يجب أن تُبرمج حركة الروبوت بحيث يميل جسمه قليلاً لينزاح مركز الجاذبية إلى داخل هذا المثلث الجديد قبل رفع الرجل.
• الثبات الديناميكي (Dynamic Stability): عندما يتحرك الروبوت الكلب بسرعة أكبر، مثل الهرولة (Trot)، فإنه يرفع رجلين متقابلتين قطرياً في نفس الوقت. في هذه الحالة، يتقلص مضلع الدعم ليصبح مجرد خط مستقيم قطري. هنا يفقد الروبوت ثباته الساكن بشكل مؤقت، ويعتمد على توازنه الحركي المستمر والقصور الذاتي لعدم السقوط، وذلك بتبديل الأرجل الملامسة للأرض بسرعة قبل أن يختل توازنه.

![img alt](https://github.com/taleensami001-lgtm/Dog-robot/blob/d93d7e31b23ef44e8e592979624ea1703fb68fe9/IMG_6013.jpeg)


### **7 / the most prominent expected problems i might face: سابعا / المشاكل المتوقع مواجهتها :**


1. Mechanical & Structural Issues

• Chassis Torsion: Since the robot is rectangular and lifts two diagonally opposite legs during movement (like in a trotting gait), the chassis is subjected to torsional forces. If the materials used are not strong enough relative to the robot's dimensions and mass, the frame may bend or twist.
• Motor Fatigue & Overheating: Using high-torque motors (such as BLDC motors) in the leg joints to lift the robot's mass requires drawing a high electrical current. This often leads to motor overheating, especially when the robot stands still for a long time and the motors must exert continuous effort to resist gravity.
• Gear Backlash: The presence of small gaps between the gear teeth in the leg joints can lead to imprecise movements and vibrations when walking, which throws off balance calculations.

2. Control & Software Issues

• Inverse Kinematics Complexity: To make the robot walk smoothly, it must be programmed to calculate the exact angles of every joint in all four legs in fractions of a second. This requires complex mathematical algorithms and highly responsive control loops.
• Sensor Drift: The robot relies on an Inertial Measurement Unit (IMU) to determine its tilt and balance. With frequent vibrations resulting from the legs striking the ground, sensor noise can interfere, causing a drift in the CoG calculations, which might lead to the robot falling.
• Latency: Any slight time delay between reading the sensors, processing the data in the microcontroller, and sending commands to the motors will result in the robot failing to regain its dynamic balance in time.

3. Power & Electrical Issues

• High Power Consumption: Dynamic movement and powerful motors drain the battery quickly, significantly reducing the robot's operating time.
• Voltage Drop: When the robot needs to make a sudden movement or stand up from the ground, the motors draw a massive spike of current all at once. This can cause a sudden drop in battery voltage, potentially leading to the microcontroller restarting or a complete system shutdown.

4. Environmental Interaction

• Slippage: If the tips of the robot's feet are not covered with a high-friction material (like rubber), it may easily slip on smooth surfaces. Slipping abruptly alters the "support polygon" area, causing the robot to lose its balance and fall.
• Unexpected Obstacles: Walking on uneven terrain requires programming the robot to react to obstacles or absorb shocks when placing a foot down. Otherwise, encountering any small bump could flip the robot over.


1. المشاكل الميكانيكية والهيكلية (Mechanical & Structural Issues)

• التواء الهيكل (Chassis Torsion): نظراً لأن الروبوت مستطيل ويرفع رجلين متعاكستين قطرياً أثناء الحركة (كما في حركة الهرولة)، يتعرض الهيكل لقوى التواء. إذا لم تكن المواد المستخدمة قوية بما يكفي مقارنة بأبعاد الروبوت وكتلته، فقد ينحني الهيكل أو يلتوي.
• إجهاد المحركات والحرارة الزائدة: استخدام محركات ذات عزم دوران عالي (مثل محركات BLDC) في مفاصل الأرجل لرفع كتلة الروبوت يتطلب سحب تيار كهربائي عالٍ. هذا يؤدي غالباً إلى ارتفاع حرارة المحركات (Overheating)، خاصة عندما يقف الروبوت ثابتاً لفترة طويلة وتضطر المحركات لبذل جهد مستمر لمقاومة الجاذبية.
• الخلوص الميكانيكي (Gear Backlash): وجود فراغات صغيرة بين أسنان التروس في مفاصل الأرجل يمكن أن يؤدي إلى حركة غير دقيقة واهتزازات عند المشي، مما 
يفسد حسابات التوازن.

2. مشاكل التحكم والبرمجة (Control & Software Issues)

• تعقيد الكينماتيكا العكسية (Inverse Kinematics): لحعل الروبوت يمشي بسلاسة، يجب برمجته لحساب الزوايا الدقيقة لكل مفصل في الأرجل الأربعة في أجزاء من الثانية، وهو ما يتطلب خوارزميات رياضية معقدة وحلقات تحكم (Control Loops) سريعة الاستجابة.
• انحراف المستشعرات (Sensor Drift): يعتمد الروبوت على وحدة القياس بالقصور الذاتي (IMU) لمعرفة ميله وتوازنه. مع كثرة الاهتزازات الناتجة عن اصطدام الأرجل بالأرض، قد تتداخل القراءات (Sensor Noise) ويحدث انحراف في حسابات مركز الجاذبية، مما قد يؤدي إلى سقوط الروبوت.
• التأخير (Latency): أي تأخير زمني بسيط بين قراءة المستشعرات، ومعالجة البيانات في المتحكم الدقيق، وإرسال الأوامر للمحركات سيؤدي إلى فشل الروبوت في استعادة توازنه الديناميكي في الوقت المناسب.

3. مشاكل الطاقة والكهرباء (Power & Electrical Issues)

• الاستهلاك العالي للطاقة: الحركة الديناميكية والمحركات القوية تستهلك طاقة البطارية بسرعة كبيرة، مما يقلل من وقت تشغيل الروبوت.
• هبوط الجهد (Voltage Drop): عند حاجة الروبوت للقيام بحركة مفاجئة أو النهوض من الأرض، تسحب المحركات تياراً عالياً جداً دفعة واحدة، مما قد يتسبب في انخفاض جهد البطارية فجأة وإعادة تشغيل (Restart) المتحكم الدقيق أو انقطاع النظام.

4. التفاعل مع البيئة (Environmental Interaction)

• الانزلاق (Slippage): إذا لم تكن أطراف أقدام الروبوت مغطاة بمادة ذات احتكاك عالي (مثل المطاط)، فقد ينزلق على الأسطح الملساء. الانزلاق يغير من مساحة "مضلع الدعم" بشكل مفاجئ، مما يجعل الروبوت يفقد توازنه ويسقط.
• الاصطدام غير المتوقع: السير على أرضيات غير مستوية يتطلب برمجة الروبوت للتفاعل مع العوائق أو امتصاص الصدمات عند وضع القدم، وإلا فإن أي نتوء صغير قد يقلب الروبوت.
