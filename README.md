# Fuzzy Ambiguity and Attention Determination
Domestic service robots have the promising potential of bringing significant services to the general population, and more importantly, successful applications of universal domestic service robots can potentially help mitigate critical societal issues such as senior care. In order to do so, domestic service robots need to integrate seamlessly into home environments. However, home environments are dynamic, complex and filled with personal items. Therefore, ambiguity can quickly arise for robots operating in such rich environments. We propose an object ambiguity determination system that can determine the level of ambiguity in robot object selection tasks with fuzzy logic data integration. Additionally, we propose a functional human attention assessment system with fuzzy logic that enables the robot to determine user attention before committing to general disambiguation processes. Our preliminary results show that the proposed fuzzy logic inference systems can reliably estimate the robot object selection task ambiguity from object confidence level and the number of potential target objects that satisfy the user's command. Furthermore, fuzzy inference is applied to decide human eye gaze direction robustly. These subsystems can be utilized in the context of human-robot interaction to guide the robot when to seek feedback from a human partner in order to disambiguate reference in domestic service tasks.

## Ambiguity Determination
 We extract the object confidence of the target object(s) and the number of items that satisfy the user command. These crisp numerical values feed the fuzzy inference system for analysis and data integration. Finally, the system computes a crisp numerical ambiguity level metric for the robot to determine the ambiguity of the current situation, and the robot can react accordingly based on the level of ambiguity. Note that the ambiguity level is a crisp value from zero to 1; a high value for this metric indicates highly ambiguous situations and vice versa. Our fuzzy decision system utilizes the object confidence score of the target object and the number of objects that satisfy the human instruction as antecedents, and the consequent of the system is the ambiguity level of the task.

## Attention Determination
Head orientation and gaze direction are key indicators of human attention. The system determines the attention level of the user. We track the locations of pupils to determine gaze direction. Because eyes are typically small compared to other facial and postural features; thus, the determination of gaze direction with naïve boolean thresholding to be unreliable. Therefore, we utilize fuzzy logic to determine eye gaze direction. 

## Requirements
Python 3.x

opencv 4.5.5 +

mediapipe 0.8.9 +

scikit-fuzzy 0.4.2


## Usage
Run fuzzyAmbiguity.py for ambiguity check

Run fuzzyAttention.py for attention determination
