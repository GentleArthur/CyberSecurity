# Introduction
Our solution won first place in a CyberSecurity competition.Our method has a higher signal-to-noise ratio compared to other methods (e.g., using CTCLoss), and this method is implemented in two main steps.As a first step, a Comparatively fine search is applied to find a subsequence that is similar to the target command.In the second step,add loss functions and control their weights only for the sequences that need to be updated.This is a very simple logic and takes only 40 minutes to 2 hours to produce each high SNR adversarial example.Information on all of the adversarial samples we have produced can be viewed in AESInfo.txt.This file includes the adversarial sample file name and the signal-to-noise ratio.The whole process can be viewed in Pseudocode.pdf.
# Usage
Our most prominent code can be seen in CEL.py.Different samples and different target orders require different number of iterations.In our code, four parameters need to be entered, including the original audio file, the target command (special note: the target command to be attacked needs to have consecutive identical letters with a '/' in the middle), the save path and the compare target command (this command is compared with the output command of the adversarial example without the '/').Of course, for the attack target command and the compare target command, we have already encapsulated them and only need to call text[i] and text_out[i].
for example:
~~~
python CEL.py --originalFile ./originalFile/01.wav --command 0 --save ./generated/carrier01_c01.wav --command_out 0
~~~
# adversarial examples
Our production confrontation samples can be downloaded in https://pan.baidu.com/s/17hpv9zPtxGixXU5-t4cfYQ，the code is "csae".
