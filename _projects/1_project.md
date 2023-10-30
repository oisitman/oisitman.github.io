---
layout: page
title: NeuRoboScope
description: Robot-assisted endoscope control that can be manipulated by surgical tools
img: assets/img/publication_preview/neuroboscope.png
importance: 3
category: Academic
related_publications: isitmanMSc,isitman2018,isitman2019,isitman19

---



| **Information**                                     | **Details**                                                                                                    |
| :-------------------------------------------------- | :------------------------------------------------------------------------------------------------------------- |
| **Funding Agency**                                  | THE SCIENTIFIC AND TECHNOLOGICAL RESEARCH COUNCIL OF TURKEY (TÜBİTAK)                                          |
| **Program**                                         | 1003                                                                                                           |
| **ID/Acronym**                                      | 115E726 / Neuroboscope                                                                                         |
| **Grant Period**                                    | 2016-2018                                                                                                      |
| **Principal Investigator**                          | Prof. Dr. M. İ. Can Dede                                                                                             |
| **Project Partners**                                | [Department of Mechanical Engineering, Izmir Institute of Technology](https://robotics.iyte.edu.tr/)<br>[Hacettepe University, Brain and Neurosurgery Department](https://hastane.hacettepe.edu.tr/81_en.html)      |
| **Project Group**                                   | Prof. Dr. M. İ. Can Dede<br>Prof. Dr. Gökhan Kiper<br>Prof. Dr. Barbaros Özdemirel<br>Prof. Dr. Enver Tatlıcıoğlu<br>Prof. Dr. Tolga Ayav<br>Omar Maaroof, PhD Student<br>Oğulcan Işıtman, MSc Student<br>Gizem Ateş, MSc Student<br>Abdullah Yaşır, MSc Student<br>Sercan Erat, MSc Student<br>Bengisu Uzun, MSc Student |

<br>

### Aim:

The Pituitary, situated between the visual nerves at the skull base, serves as a crucial gland. The NeuRoboScope project aims to create a specialized robotic system to support endoscopic pituitary surgeries. These surgeries address pathologies originating from the pituitary gland. The proposed system intends to empower surgeons to operate three distinct tools concurrently, including an endoscope. This simultaneous operation is anticipated to enhance surgical productivity and reduce operation duration. The system includes a central control unit that attaches to non-endoscope surgical tools, capturing and processing the surgeon's hand motions. The processed information is then transmitted to the robot managing the endoscope. This design allows the surgeon to control the endoscope seamlessly while employing other surgical tools with both hands throughout the procedure.

<br>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/publication_preview/neuroboscope.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
     Teleoperatively manipulated robotic endoscope holder 
</div>

### Short Summary of the Topic:

The pituitary, a crucial gland regulating hormonal balance, directly or indirectly influences the functioning of all body organs through its control over essential fluids. Pathologies around the pituitary pose significant health risks due to its vital role. Treatment for such tumors involves either skull-opening procedures or non-invasive methods like endoscopic transnasal transsphenoidal surgery. This modern and effective pituitary surgery employs an endoscope, a tool projecting strong light for illumination and providing a two-dimensional video display of the operative area.

Despite its advantages, the endoscopic procedure presents challenges. Operating the endoscope with one hand, especially given its weight compared to other tools, fatigues the surgeon during the typically lengthy 2-3 hour procedure. This limitation extends operation times and compromises surgical success. Surgeons also need to use multiple tools simultaneously, requiring assistance, yet coordinating with an assistant operating the endoscope poses difficulties, affecting surgical performance.

To address these issues, a system is essential to hold and guide the endoscope effectively. Although various endoscope holders exist, they often fall short of clinical needs and lack widespread adoption. This project endeavors to develop an innovative robotic system to meet these specific clinical requirements and enhance the efficiency of endoscopic pituitary surgeries.


<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/neuroboscope.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/neuroboscope_2.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

### Organizational Approach and the main structure of the Method:

Initially, expert surgeons specialized in endoscopic pituitary surgery will gather anatomical, radiological, and surgical information, along with defining system requirements. Given that the proposed system is a robotics application, it necessitates an interdisciplinary approach, incorporating mechanical, electrical, electronics, and software fields. The focus of this project lies in the field of mechanism science to design a surgery robot mechanism characterized by high precision, back-driveability, and equilibrium against gravitational effects for overall system safety.

The operational mode involves teleoperation, wherein inputs from the surgical tool guide the robot managing the endoscope. System dynamics and control will be the focal point for developing the teleoperation system. Embedded coding studies will be conducted to implement the developed control algorithms on controller cards. This encompasses data acquisition and signal processing efforts to regulate real-time data transfer among subsystems (sensors, actuators, controller cards, etc.).

The surgical team's involvement is crucial in contributing to the development of 3D anatomical models, simulation environments, and end-user evaluations for designs on anatomical models and cadavers. While preclinical tests, including precision measurements and end-user evaluations on simulated anatomical models and cadavers, are part of the project scope, clinical tests are deferred until after the project's completion due to the risky and highly critical nature of the operation. Clinical tests will be contingent on the results of preclinical evaluations conducted within the project's timeframe.

### On How to contribute to the goals and targets of the call program with the expected targets and outcomes of the project:

This project aims to guide the optical-camera system in endoscopic pituitary surgery by tracking the surgeon's tool. The skills learned in mechanics, electronics, and software will be applied to future surgical robotics projects. The goal is to create a robotics system for minimally invasive surgery, aligning with the program's objectives. The overall system architecture developed in this project will also support robot-assisted surgeries in other similar procedures.
<br>
<br>
**For the most up-to-date information on this project, please check out the [Iztech Robotics Lab](https://robotics.iyte.edu.tr/).**