<h1>VirtualBox – How To Connect A Windows OS Host-Only Client Virtual Machine To A Windows Server NAS Virtual Machine’s Active Directory Domain</h1>


<h2 style="font-family: Arial, sans-serif; font-size: 20px; font-weight: bold; margin-top: 24px; margin-bottom: 12px;">
⏹️ Description</h2>

<p style="font-family: Georgia, serif; font-size: 16px; margin-top: 12px; margin-bottom: 12px;">
In this project, a Windows 11 host-only client virtual machine is connected to a Windows Server 2025 NAS virtual machine’s Active Directory domain. You will configure the Windows 11 client to join the existing Active Directory domain, rename the client computer appropriately, and verify that the device is successfully added to the domain environment. To complete this task, you will open the Windows 11 system settings, access the computer name and domain configuration settings, select the domain option, and enter the Active Directory domain name. You will then rename the client computer, provide domain administrator credentials to authorize the join, restart the client computer to apply the changes, confirm the computer object appears in Active Directory Users and Computers on the Windows Server, and sign in to the Windows 11 client using a domain administrator account. After the configuration is completed successfully, the Windows 11 client becomes joined to the Active Directory domain and appears in the Computers folder within Active Directory Users and Computers. You will also be able to confirm domain connectivity from the Windows 11 sign-in screen and log in with a domain-based administrator account.
</b>



<h2 style="font-family: Arial, sans-serif; font-size: 20px; font-weight: bold; margin-top: 24px; margin-bottom: 12px;">
⏹️ Utilities Used</h2>
  
<p style="font-family: Georgia, serif; font-size: 16px; margin-top: 12px; margin-bottom: 12px;">
 
 - <b>VirtualBox, Settings, Active Directory Users and Computers</b>



<h2 style="font-family: Arial, sans-serif; font-size: 20px; font-weight: bold; margin-top: 24px; margin-bottom: 12px;"> 
⏹️ Environments Used </h2>

<p style="font-family: Georgia, serif; font-size: 16px; margin-top: 12px; margin-bottom: 12px;">
 
- <b>VirtualBox, Windows Server 2025, Windows 11 Pro</b>



<h2 style="font-family: Arial, sans-serif; font-size: 20px; font-weight: bold; margin-top: 24px; margin-bottom: 12px;"> 
<h2>
⏹️ Project Walk-Through:</h2>
 <br/>

</div>
  <span style="font-family: Arial, sans-serif; font-size: 16px;"><b>WINDOWS 11 – CLIENT COMPUTER SETUP</b></span>  
<br/><br/>


</div>
  <span style="font-family: Arial, sans-serif; font-size: 16px;"><b>Right-Click: Start. Select System.</b></span>  
<br/><br/>

<table>
  <tr>
    <td><img src="https://imgur.com/bhQOu8p.png" height="50%" width="50%" /></td>
    <td><img src="https://imgur.com/CCSVOQm.png" height="100%" width="100%" /></td>
  </tr>
</table>

<br /><br />


</div>
  <span style="font-family: Arial, sans-serif; font-size: 16px;"><b>You will be in: System – About. Click: Domain or workgroup (blue, next to: Related links).</b></span>  
<br/><br/>

<table>
  <tr>
    <td><img src="https://imgur.com/NhfC0H8.png" height="100%" width="100%" /></td>
  </tr>
</table>

<table>
  <tr>
    <td><img src="https://imgur.com/0xLGWwS.png" height="100%" width="100%" /></td>
  </tr>
</table>

<br /><br />


</div>
  <span style="font-family: Arial, sans-serif; font-size: 16px;"><b>A box will pop-up called: System Properties. Click: Change (under: Network ID).</b></span>  
<br/><br/>

<table>
  <tr>
    <td><img src="https://imgur.com/NjlaI8U.png" height="50%" width="50%" /></td>
  </tr>
</table>

<table>
  <tr>
    <td><img src="https://imgur.com/UfhNgT1.png" height="75%" width="75%" /></td>
    <td><img src="https://imgur.com/Wc79pOL.png" height="100%" width="100%" /></td>
  </tr>
</table>

<br /><br />


</div>
  <span style="font-family: Arial, sans-serif; font-size: 16px;"><b>A box will pop-up called: Computer Name/Domain Changes. Click/Select: Domain (above: Workgroup). Type: The domain you want to connect to on Active Directory Users and Computers (ex: corp.rashaditlabs.com). Click: OK. If successful, go to: WINDOWS 11 – CLIENT COMPUTER SETUP CONTINUED.</b></span> 
<br/><br/>

<table>
  <tr>
    <td><img src="https://imgur.com/YjG4cWX.png" height="50%" width="50%" /></td>
  </tr>
</table>

<table>
  <tr>
    <td><img src="https://imgur.com/UZbHBDB.png" height="75%" width="75%" /></td>
    <td><img src="https://imgur.com/X5OvRdT.png" height="100%" width="100%" /></td>
  </tr>
</table>

<br /><br />


</div>
  <span style="font-family: Arial, sans-serif; font-size: 16px;"><b>HOW TO SOLVE THE ERROR: “…A general network error occurred.” – PART ONE – WINDOWS 11</b></span> 
<br/><br/>

</div>
  <span style="font-family: Arial, sans-serif; font-size: 16px;"><b>If you get this error: “…A general network error occurred.”. Click: OK. Disconnect the firewall by: Open: Windows Defender Firewall with Advanced Security.</b></span> 
<br/><br/>

<table>
  <tr>
    <td><img src="https://imgur.com/xcxIAU2.png" height="75%" width="75%" /></td>
    <td><img src="https://imgur.com/BzmjGR4.png" height="100%" width="100%" /></td>
  </tr>
</table>

<table>
  <tr>
    <td><img src="https://imgur.com/KJwyN3D.png" height="75%" width="75%" /></td>
  </tr>
</table>

<br /><br />


</div>
  <span style="font-family: Arial, sans-serif; font-size: 16px;"><b>In Windows Defender Firewall with Advanced Security, Click: Properties (far-right column called: Actions, between: Refresh and Help).</b></span> 
<br/><br/>

</div>
  <span style="font-family: Arial, sans-serif; font-size: 16px;"><b>•	NOTE: Only because this is a lab, you can keep the firewalls off if you if you want. It is a lot better to turn the firewalls back on after joining the Active Directory User and Computer domain.</b></span> 
<br/><br/>

<table>
  <tr>
    <td><img src="https://imgur.com/kM7KYts.png" height="75%" width="75%" /></td>
  </tr>
</table>

<table>
  <tr>
    <td><img src="https://imgur.com/G5D8Ltd.png" height="75%" width="75%" /></td>
    <td><img src="https://imgur.com/kQ5xTvN.png" height="100%" width="100%" /></td>
  </tr>
</table>

<br /><br />


</div>
  <span style="font-family: Arial, sans-serif; font-size: 16px;"><b>A box will pop-up called: Windows Defender Firewall with Advanced Security on Local Computer, Domain Profile tab. Click: The box to the right of: Firewall state, Select: Off.</b></span> 
<br/><br/>

<table>
  <tr>
    <td><img src="https://imgur.com/ZTeaJTc.png" height="50%" width="50%" /></td>
  </tr>
</table>

<table>
  <tr>
    <td><img src="https://imgur.com/96pGyZh.png" height="75%" width="75%" /></td>
    <td><img src="https://imgur.com/mJKTlXC.png" height="100%" width="100%" /></td>
  </tr>
</table>

<br /><br />


</div>
  <span style="font-family: Arial, sans-serif; font-size: 16px;"><b>Click/Select: Private Profile tab (top, next to: Domain Profile). Click: The box to the right of: Firewall state, Select: Off.</b></span> 
<br/><br/>

<table>
  <tr>
    <td><img src="https://imgur.com/KdrT6J9.png" height="100%" width="100%" /></td>
    <td><img src="https://imgur.com/jIX7JJ0.png" height="100%" width="100%" /></td>
  </tr>
</table>

<br /><br />


</div>
  <span style="font-family: Arial, sans-serif; font-size: 16px;"><b>Click/Select: Public Profile tab (top, next to: Domain Profile). Click: The box to the right of: Firewall state, Select: Off.</b></span> 
<br/><br/>

<table>
  <tr>
    <td><img src="https://imgur.com/a2Yeq3q.png" height="100%" width="100%" /></td>
    <td><img src="https://imgur.com/OQB23fO.png" height="100%" width="100%" /></td>
  </tr>
</table>

<br /><br />


</div>
  <span style="font-family: Arial, sans-serif; font-size: 16px;"><b>Click: Apply (bottom-right corner). Click: OK.</b></span> 
<br/><br/>

<table>
  <tr>
    <td><img src="https://imgur.com/xdmljUH.png" height="50%" width="50%" /></td>
  </tr>
</table>

<table>
  <tr>
    <td><img src="https://imgur.com/athnXuR.png" height="100%" width="100%" /></td>
    <td><img src="https://imgur.com/f1QRRPl.png" height="100%" width="100%" /></td>
  </tr>
</table>

<br /><br />


</div>
  <span style="font-family: Arial, sans-serif; font-size: 16px;"><b>Restart the Windows 11 Virtual Machine.</b></span> 
<br/><br/>

<table>
  <tr>
    <td><img src="https://imgur.com/3JEuTX4.png" height="100%" width="100%" /></td>
    <td><img src="https://imgur.com/rSHjWpu.png" height="100%" width="100%" /></td>
  </tr>
</table>

<br /><br />


</div>
  <span style="font-family: Arial, sans-serif; font-size: 16px;"><b>HOW TO SOLVE THE ERROR: “…A general network error occurred.” – PART TWO – WINDOWS 11</b></span> 
<br/><br/>

</div>
  <span style="font-family: Arial, sans-serif; font-size: 16px;"><b>Go back to the pop-up box called: Computer Name/Domain Changes. Click: OK. If you still get the error: “…A general network error occurred.”. Click: OK. Go to the next fix. If successful, go to: WINDOWS 11 – CLIENT COMPUTER SETUP CONTINUED.</b></span> 
<br/><br/>

<table>
  <tr>
    <td><img src="https://imgur.com/kEaeqTq.png" height="50%" width="50%" /></td>
    <td><img src="https://imgur.com/Vs3lqqi.png" height="75%" width="75%" /></td>
  </tr>
</table>

<table>
  <tr>
    <td><img src="https://imgur.com/0cVCsmy.png" height="75%" width="75%" /></td>
    <td><img src="https://imgur.com/5oPrPvj.png" height="100%" width="100%" /></td>
    <td><img src="https://imgur.com/6D3BOcK.png" height="100%" width="100%" /></td>
  </tr>
</table>

<br /><br />


</div>
  <span style="font-family: Arial, sans-serif; font-size: 16px;"><b>HOW TO SOLVE THE ERROR: “…A general network error occurred.” – PART THREE – WINDOWS SERVER 2025</b></span> 
<br/><br/>

</div>
  <span style="font-family: Arial, sans-serif; font-size: 16px;"><b>Open: External (NAT) Properties.</b></span> 
<br/><br/>

<table>
  <tr>
    <td><img src="https://imgur.com/s0d9SlF.png" height="100%" width="100%" /></td>
    <td><img src="https://imgur.com/7hfP4XH.png" height="100%" width="100%" /></td>
  </tr>
</table>

<table>
  <tr>
    <td><img src="https://imgur.com/J614WMx.png" height="100%" width="100%" /></td>
    <td><img src="https://imgur.com/7hfP4XH.png" height="100%" width="100%" /></td>
  </tr>
</table>

<table>
  <tr>
    <td><img src="https://imgur.com/eGk4SGt.png" height="100%" width="100%" /></td>
  </tr>
</table>

<table>
  <tr>
    <td><img src="https://imgur.com/Aw1lPJ2.png" height="100%" width="100%" /></td>
    <td><img src="https://imgur.com/MBohj7S.png" height="100%" width="100%" /></td>
  </tr>
</table>

<table>
  <tr>
    <td><img src="https://imgur.com/bN09ZkF.png" height="50%" width="50%" /></td>
  </tr>
</table>

<br /><br />


</div>
  <span style="font-family: Arial, sans-serif; font-size: 16px;"><b>Click: Internet Protocol Version 4 (TCP/IPv4). Click: Properties (next to: Uninstall).</b></span> 
<br/><br/>

<table>
  <tr>
    <td><img src="https://imgur.com/bN09ZkF.png" height="75%" width="75%" /></td>
    <td><img src="https://imgur.com/zCiFXL3.png" height="100%" width="100%" /></td>
  </tr>
</table>

<br /><br />


</div>
  <span style="font-family: Arial, sans-serif; font-size: 16px;"><b>You will be taken to a pop-up box called: Internet Protocol Version 4 (TCP/IPv4) Properties. Click: Advanced (bottom-right).</b></span> 
<br/><br/>

<table>
  <tr>
    <td><img src="https://imgur.com/fDdSeZY.png" height="75%" width="75%" /></td>
    <td><img src="https://imgur.com/2BKtzCO.png" height="100%" width="100%" /></td>
  </tr>
</table>

<br /><br />


</div>
  <span style="font-family: Arial, sans-serif; font-size: 16px;"><b>You will be taken to a pop-up box called: Advanced TCP/IP Settings, IP Settings tab. Click: DNS tab (top, between: IP Settings and WINS).</b></span> 
<br/><br/>

<table>
  <tr>
    <td><img src="https://imgur.com/NywuaKT.png" height="75%" width="75%" /></td>
    <td><img src="https://imgur.com/ol98nA5.png" height="100%" width="100%" /></td>
  </tr>
</table>

<br /><br />


</div>
  <span style="font-family: Arial, sans-serif; font-size: 16px;"><b>On the DNS tab, Click / Uncheck: Register this connection’s addresses in DNS (bottom-left, under section: DNS suffix for this connection). Click: OK.</b></span> 
<br/><br/>

</div>
  <span style="font-family: Arial, sans-serif; font-size: 16px;"><b>•	NOTE: This prevents the internet-facing NIC from advertising itself as an Active Directory address. Only the internal/domain NIC should publish domain controller DNS records.</b></span> 
<br/><br/>

<table>
  <tr>
    <td><img src="https://imgur.com/HoOMhGl.png" height="50%" width="50%" /></td>
  </tr>
</table>

<table>
  <tr>
    <td><img src="https://imgur.com/Xq74dRo.png" height="75%" width="75%" /></td>
    <td><img src="https://imgur.com/nnARzZi.png" height="100%" width="100%" /></td>
  </tr>
</table>

<br /><br />


</div>
  <span style="font-family: Arial, sans-serif; font-size: 16px;"><b>You will be taken back to a pop-up box called: Internet Protocol Version 4 (TCP/IPv4) Properties. Click: Close.</b></span> 
<br/><br/>

<table>
  <tr>
    <td><img src="https://imgur.com/bN09ZkF.png" height="50%" width="50%" /></td>
    <td><img src="https://imgur.com/LTdfEsL.png" height="100%" width="100%" /></td>
  </tr>
</table>

<br /><br />


</div>
  <span style="font-family: Arial, sans-serif; font-size: 16px;"><b>Restart the Windows 11 Virtual Machine.</b></span> 
<br/><br/>

<table>
  <tr>
    <td><img src="https://imgur.com/3JEuTX4.png" height="75%" width="75%" /></td>
    <td><img src="https://imgur.com/rSHjWpu.png" height="100%" width="100%" /></td>
  </tr>
</table>

<br /><br />


</div>
  <span style="font-family: Arial, sans-serif; font-size: 16px;"><b>HOW TO SOLVE THE ERROR: “…A general network error occurred.” – PART FOUR – WINDOWS 11</b></span> 
<br/><br/>

</div>
  <span style="font-family: Arial, sans-serif; font-size: 16px;"><b>Go back to the pop-up box called: Computer Name/Domain Changes. Click: OK. If you still get the error: “…A general network error occurred.”. Click: OK. Go to the next fix. If successful, go to: WINDOWS 11 – CLIENT COMPUTER SETUP CONTINUED.</b></span> 
<br/><br/>

<table>
  <tr>
    <td><img src="https://imgur.com/kEaeqTq.png" height="50%" width="50%" /></td>
    <td><img src="https://imgur.com/Vs3lqqi.png" height="75%" width="75%" /></td>
  </tr>
</table>

<table>
  <tr>
    <td><img src="https://imgur.com/0cVCsmy.png" height="75%" width="75%" /></td>
    <td><img src="https://imgur.com/5oPrPvj.png" height="100%" width="100%" /></td>
    <td><img src="https://imgur.com/6D3BOcK.png" height="100%" width="100%" /></td>
  </tr>
</table>

<br /><br />


</div>
  <span style="font-family: Arial, sans-serif; font-size: 16px;"><b>Open: Command Prompt. 1) Run command: ipconfig /flushdns  . 2) Run command: ipconfig /registerdns  . 3) Run command: net stop netlogon  . 4) Run command: ex: net start netlogon  .</b></span> 
<br/><br/>

<table>
  <tr>
    <td><img src="https://imgur.com/1nApdzs.png" height="100%" width="100%" /></td>
    <td><img src="https://imgur.com/Vs3lqqi.png" height="100%" width="100%" /></td>
  </tr>
</table>

<table>
  <tr>
    <td><img src="https://imgur.com/0cVCsmy.png" height="50%" width="50%" /></td>
  </tr>
</table>

<table>
  <tr>
    <td><img src="https://imgur.com/kEaeqTq.png" height="100%" width="100%" /></td>
    <td><img src="https://imgur.com/Vs3lqqi.png" height="100%" width="100%" /></td>
  </tr>
</table>

<br /><br />
