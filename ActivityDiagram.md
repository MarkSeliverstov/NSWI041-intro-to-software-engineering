## Activity diagram for changing email address

```
@startuml
|User|
start
repeat 

:Sign in;
|#AntiqueWhite|SIS|
:Verify Credentials;
repeat while (verified?) is (No) not (Yes)

|User|
:Show menu;
:Go to Personal Data;
|SIS|
:Load Personal data module;
|User|
:Edit;

:Edit mail addr;
:Save edited data;
|SIS|
:Changed Data (must be inbetween)>
:Validate Format;
if (valid?) then (yes)
:Send Verification Mail to the mail addr;
|User|
:Verify mail;
|SIS|
if (verified?) then (yes)
:Save Changes;
:Notify User about success;
else (no)
stop
endif
else (no)
|SIS|
:Notify about failure;
endif
|User|
:Receive notification;
stop
@enduml
```
![PL3Tojim3BttKmXsaxn23DitkXy6MnaBszYb6okDmB4wMsufvE4dDoGTV5V6EZe_HozPN98o1xFyp9WMy_YRX1Tq0iPqFPqZKBHcUVC-2lqj-7iYmQN_qY-c-uM9nZiS4dfKr8LiD-vjee3GNEi6eN_N0cLeZjn2P87c3-RMRAPTF_4DPep5ckupWp1ynvGvkW0Vd3XrN_s-ilDFo2i4C_iIqEvI7ps9DUiBiwC0pljarSDT4L2dwC7_Bt](https://github.com/MarkSeliverstov/NSWI041-intro-to-software-engineering/assets/120932204/c87da3b5-533d-42c0-9b1e-b035f1dfbd50)


