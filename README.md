# Niagara-4-FRPC-Module
Through this module, an FRPC mapping service can be deployed in the Niagara Station, enabling users to remotely access the Niagara site. Trial mode allows 30 days of free use after each station start. Welcome to use it free for remote project deployment. 
<img width="962" height="268" alt="image" src="https://github.com/user-attachments/assets/ec5c4706-16ce-4672-841e-9c523507fb5a" />
This FRPC module can enable cloud port mapping within Niagara, directly exposing the intranet ports of the Niagara station to the cloud. It has been tested to support automatic reconnection upon network interruptions—meaning it will reconnect if the network is temporarily disrupted. Please note: if the station reboots, this FRPC service will not reconnect automatically; you will need to deploy an additional program to check whether the cloud port is functioning properly. We have verified compatibility with N4.14 on JACE, Edge, and Windows-based Niagara supervisors.

Here, we provide an additional program to check whether the FRPC cloud port is valid. If the mapped cloud port is port 80 of the JACE, you can use our program. Open CurlCommand_check_FRPC_Port.bog with Workbench. If the trigger is a web page file, you will see the result.
<img width="570" height="84" alt="image" src="https://github.com/user-attachments/assets/dede303f-e6da-47aa-ad8d-9d1fe84e85a3" />


<img width="382" height="118" alt="image" src="https://github.com/user-attachments/assets/04ccf2fd-1d33-4edd-ad63-93fe363f8493" />

After gline.pem is added to your user trust store, simply drag and drop the glineFrpc module into the wiresheet, and it will be ready to use.
<img width="786" height="106" alt="image" src="https://github.com/user-attachments/assets/ee2701db-2533-486e-bbaf-451bb6069f77" />

Logs can also be read in Niagara's Application Director.
If you are interested, please contact: jason.zhang@gline-net.com or WhatsApp +8613801909968.
