The objective is to explore the medicare data for inpatient and outpatient care. 
Data included in this project:
1. Inpatient_provdr.csv
2. Outpatient_provdr.csv

According to https://www.sgu.edu/blog/medical/inpatient-versus-outpatient. Inpatient, in the most basic sense, refers to someone admitted to the hospital to stay overnight, whether briefly or for an extended period of time. Physicians keep these patients at the hospital to monitor them more closely. Outpatient care, also called ambulatory care, defines any service or treatment that doesn’t require hospitalization. An annual exam with your primary care physician is an example of outpatient care, but so are emergent cases where the patient leaves the emergency department the same day they arrive. Any appointment at a clinic or specialty facility outside the hospital is considered outpatient care as well. While there’s a clear difference between an inpatient and an outpatient, there is a little bit of gray area as well. Occasionally, physicians will assign a patient observation status while they determine whether hospitalization is required. This period typically lasts for no more than 24 hours. Also note that the location itself doesn’t define whether you’re an inpatient versus outpatient. It’s the duration of stay, not the type of establishment, that determines your status.

The project has been broken into three diffrent Jupyter Notebooks:
1. inpatientData.ipynb
2. outpatientData.ipynb
3. inpatient_outpatient_comparison.ipynb

The following are some examples of questions we tried to analyze and visualize in our Jupyter Notebook: 
* Visualize and compare the inpatient/outpatient total average payment ratio among different states.

Average Total Payments for outpatient care in each States
![outpatient_avergae_total_payment](https://user-images.githubusercontent.com/63881504/205670509-8c0a88aa-c0e2-4e4e-969c-06e0098a1b08.png)

Average Total Payments for inpatient care in each States
![inpatient_avergae_total_payment](https://user-images.githubusercontent.com/63881504/205670539-71f0a44d-661a-4370-807b-e7bfd14b3f3a.png)

* Visualize and compare the cost of the same procedure among different states.
![ranked_outpatient_cost_procedure](https://user-images.githubusercontent.com/63881504/205669528-87f94b56-d879-4723-a195-cf00ceec3ba0.png)

_Ranked Outpatient Procedure Observations_
* Wyoming (WY) is the state with the most expensive outpatient procedures (total = 11 at HIGH LEVEL).
* Arkansas (AK) is the second state with the most expensive outpatient procedures (total = 8 at HIGH LEVEL).
* MA, CA, NY, and VT have very low cost per outpatient procedures.Perhaps they have laws that cap-out procedures at certain prices due to political standings of the states on public health. 
* WA, RI, OR, NH, IA, GA, and DC all have very low to average outpatient cost per procedure except for procedure 0203 (Level IV Nerve Injection). This particular outpatient procedure might be consider very expensive because of the stem cell therapy used for spine injuries. 

![ranked_inpatient_cost_procedure](https://user-images.githubusercontent.com/63881504/205669494-f0f85327-d069-4f9b-9e3c-9250882ff2ce.png)

_Ranked Inpatient Procedure Observations_
* Arkansas (AK) is the state with the most expensive inpatient procedures (total = 22 at HIGH LEVEL).
* Wyoming (WY) is the second state with the most expensive inpatient procedures (total = 13 at HIGH LEVEL).
* Hawaii (HI) is the third state with the most expensive procedures (total = 12 at HIGH LEVEL).
* MD, MA, NY, DC, CT, and CA have very low cost per inpatient procedures.Perhaps they have laws that cap-out procedures at certain prices due to political standings of the states on public health. 
* Most of VT procedures are very low priced except for 149 (DYSEQUILIBRIUM), 203(BRONCHITIS & ASTHMA), 301(PERIPHERAL VASCULAR DISORDERS), 303(ATHEROSCLEROSIS), 305(HYPERTENSION), and 811(RED BLOOD CELL DISORDERS). Perhaps these procedures are more expensive for states as VT since these are almost all heart related diseases which need more treatments, more medications, and more diagnosis from doctors. 

* List the top 10 most common outpatient/inpatient procedures.
   
|  Outpatient Procedure Name                                                            |Count   |  
|---------------------------------------------------------------------------------------|--------|
|0267 - Level III Diagnostic and Screening Ultrasound                                   |2998    |   
|0269 - Level II Echocardiogram Without Contrast                                        |2304    |   
|0336 - Magnetic Resonance Imaging and Magnetic Resonance Angiography without Contrast  |2248    |  
|0265 - Level I Diagnostic and Screening Ultrasound                                     |2210    |
|0377 - Level II Cardiac Imaging                                                        |2564    |
|0078 - Level III Pulmonary Treatment                                                   |2304    |
|0368 - Level II Pulmonary Tests                                                        |2248    |
|0604 - Level 1 Hospital Clinic Visits                                                  |2210    |
|0605 - Level 2 Hospital Clinic Visits                                                  |2116    |
|0207 - Level III Nerve Injections                                                      |2002    |

|  Inpatient Procedure Name                                                             |Count   |  
|---------------------------------------------------------------------------------------|--------|
|194 - SIMPLE PNEUMONIA & PLEURISY W CC                                                 |3023    |   
|690 - KIDNEY & URINARY TRACT INFECTIONS W/O MCC                                        |2989    |   
|292 - HEART FAILURE & SHOCK W CC                                                       |2953    |  
|392 - ESOPHAGITIS, GASTROENT & MISC DIGEST DISORDERS W/O MCC                           |2950    |
|641 - MISC DISORDERS OF NUTRITION,METABOLISM,FLUIDS/ELECTROLYTES W/O MCC               |2899    |
|871 - SEPTICEMIA OR SEVERE SEPSIS W/O MV 96+ HOURS W MCC                               |2812    |
|603 - CELLULITIS W/O MCC                                                               |2807    |
|470 - MAJOR JOINT REPLACEMENT OR REATTACHMENT OF LOWER EXTREMITY W/O MCC               |2750    |
|191 - CHRONIC OBSTRUCTIVE PULMONARY DISEASE W CC                                       |2750    |
|190 - CHRONIC OBSTRUCTIVE PULMONARY DISEASE W MCC                                      |2713    |


* List and compare the top 10 expensive outpatient and inpatient care.
  
| Outpatient - APC                                                                       |Average Total Payments |
|----------------------------------------------------------------------------------------|-----------------------|                                                   
|0377 - Level II Cardiac Imaging                                                         |1.917435e+06           |
|0209 - Level II Extended EEG, Sleep, and Cardiovascular Studies                         |1.487586e+06           |
|0269 - Level II Echocardiogram Without Contrast                                         |1.149260e+06           |
|0207 - Level III Nerve Injections                                                       |1.005250e+06           |
|0336 - Magnetic Resonance Imaging and Magnetic Resonance Angiography without Contrast   |9.962915e+05           |
|0270 - Level III Echocardiogram Without Contrast                                        |6.536593e+05           |
|0020 - Level II Excision/ Biopsy                                                        |6.028816e+05           |
|0074 - Level IV Endoscopy Upper Airway                                                  |6.015580e+05           |
|0267 - Level III Diagnostic and Screening Ultrasound                                    |4.535527e+05           |
|0204 - Level I Nerve Injections                                                         |2.940389e+05           |

|Inpatient - DRG Definition                                                              |Average Total Payments |
|----------------------------------------------------------------------------------------|-----------------------|                                                   
|329 - MAJOR SMALL & LARGE BOWEL PROCEDURES W MCC                                        |5.574202e+07           |
|853 - INFECTIOUS & PARASITIC DISEASES W O.R. PROCEDURE W MCC                            |5.547477e+07           |
|207 - DEGENERATIVE NERVOUS SYSTEM DISORDERS W/O MCC                                     |4.487892e+07           |                                                     
|870 - SEPTICEMIA OR SEVERE SEPSIS W MV 96+ HOURS                                        |4.155966e+07           |
|470 - MAJOR JOINT REPLACEMENT OR REATTACHMENT OF LOWER EXTREMITY W/O MCC                |4.005907e+07           |
|871 - SEPTICEMIA OR SEVERE SEPSIS W/O MV 96+ HOURS W MCC                                |3.722758e+07           |
|460 - SPINAL FUSION EXCEPT CERVICAL W/O MCC                                             |3.231312e+07           |
|208 - ESPIRATORY SYSTEM DIAGNOSIS W VENTILATOR SUPPORT <96 HOURS                        |3.015266e+07           |
|330 - MAJOR SMALL & LARGE BOWEL PROCEDURES W CC                                         |2.940389e+05           |
|291 - HEART FAILURE & SHOCK W MCC                                                       |2.758622e+07           |