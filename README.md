DCAS MQTT Publisher.exe 

README  |  Version 2.9 

IMPORTANT: COMMUNITY TOOL - NOT AN OFFICIAL DISTECH CONTROLS PRODUCT 

This application is a community-driven project created by members of the Distech Controls Advanced Support Team and is not a sanctioned or official Distech Controls release. Read the accompanying disclaimer before using this tool. 

Overview 

DCAS MQTT Publisher.exe is a Windows-based MQTT publishing utility for configuring brokers, managing topics, publishing MQTT messages, retrieving live oBIX values, and automating interval-based or change-based publishing. It includes TLS and client-certificate options, diagnostic logging, and CSV import/export. 

Key Features 

•  Multiple MQTT broker profiles with configurable address, port, authentication, TLS, client ID, clean session, keep-alive, and Last Will settings 

•  MQTT publishing with QoS 0, 1, and 2 plus retained-message support 

•  Manual publishing of selected topics or all configured topics 

•  Interval publishing with an initial full publish followed by changed-value publishing 

•  oBIX data retrieval using HTTP Basic authentication and optional recurring polling 

•  Live linking of oBIX values to MQTT topics and refresh before publication 

•  CSV import and export for MQTT topic configuration 

•  Automatic configuration saving under the active Windows user profile 

•  Expandable diagnostic log with copy and clear functions 

•  Broker connection testing with detailed TCP, TLS, MQTT CONNECT, and CONNACK diagnostics 

System Requirements 

•  Windows 10 or Windows 11 

•  Windows PowerShell 5.1 or a compatible packaged executable environment 

•  Network access to the configured MQTT broker and any configured oBIX endpoint 

•  Appropriate broker, topic, oBIX, firewall, certificate, and network permissions 

Installation 

1. Place DCAS MQTT Publisher.exe in a folder where the user has permission to run applications. 

2. If supplied, keep the README and disclaimer with the executable. 

3. Launch DCAS MQTT Publisher.exe under the Windows account that will own the saved configuration. 

4. Review the disclaimer and validate the tool in a controlled environment before production use. 

Usage Summary 

1. Open the Brokers tab and add a broker name, address, port, and required security settings. 

2. Select the saved broker and use Test Connection to verify TCP, TLS, and MQTT connectivity. 

3. Open the Topics tab and add the topic, optional subtopic, payload, broker, QoS, and retain setting. 

4. Use Publish Selected or Publish All for manual publication. 

5. Optionally configure an interval and start interval publishing. The first interval cycle publishes all configured topics; later cycles publish changed values only. 

6. For live data, open the oBIX tab, enter the endpoint and credentials, fetch data, then send selected values to the Topics list. 

7. Use the Diagnostic Log panel to review connection, synchronization, and publishing activity. 

Configuration and Data Storage 

The application saves its configuration as config.json in the MqttTopicPublisher folder under the active user’s Windows application-data directory. Broker settings, topic mappings, oBIX settings, publish intervals, and auto-start preferences can be retained between sessions. 

Security notice: the current script stores broker passwords, client-certificate passwords, and oBIX credentials in the configuration data without application-level encryption. Protect the Windows account, configuration folder, exported CSV files, certificates, screenshots, and logs. 

Important Operational Notes 

•  Validate topic paths, payloads, QoS, retain settings, broker selection, and oBIX mappings before publishing. 

•  Use least-privilege broker and oBIX accounts whenever possible. 

•  Automatic publishing can send values repeatedly and can affect connected subscribers or downstream automation. 

•  The Allow invalid certificate options weaken certificate validation and should be used only in controlled, explicitly approved environments. 

•  Diagnostic logs may contain addresses, endpoint paths, topic names, and error details. Review and redact logs before sharing. 

•  Test with non-critical topics and maintain a rollback plan before production deployment. 

Troubleshooting 

•  If a broker test fails, expand the Diagnostic Log and identify whether the failure occurred during TCP connection, TLS negotiation, MQTT CONNECT transmission, or CONNACK processing. 

•  Confirm that the broker address contains only the host name or IP address and that the configured port matches the TLS setting. 

•  For authentication failures, verify the username, password, client ID, topic permissions, and certificate configuration. 

•  If oBIX returns a login page or HTTP error, verify the endpoint URL, credentials, certificate trust, and server permissions. 

•  If values are not changing, verify the oBIX source path, polling interval, topic link, and current payload shown in the Topics grid. 

Legal and Support 

•  Community tool provided as is and without warranty. 

•  Not an official Distech Controls product. 

•  Not covered by official product warranty, standard support agreements, or service level agreements. 

•  Support and future development are discretionary and not guaranteed. 

•  Read DCAS_MQTT_Publisher_Disclaimer.docx before use. 

 

Application 

DCAS MQTT Publisher.exe 

Version 

2.9 

Status 

Community Tool 

README Version 

1.0 

