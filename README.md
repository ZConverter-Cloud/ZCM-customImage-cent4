

OCI Migration (centos 4 custom-image)
============
>**ZConverter Cloud Migration Membership**
>
> **How to use ZConverter Cloud Migration**
>
> **Target VM generation**

## ZConverter Cloud Migration Membership

   1. **Access https://www.z-cloud.net/ through a web browser.**

![z-cloud_login_page](https://raw.githubusercontent.com/zconverter/ZCM-legacy/master/image/z-cloud/login_page.png)

   2. **Click "Register a new membership" and proceed with membership registration.**

![join](https://raw.githubusercontent.com/zconverter/ZCM-legacy/master/image/z-cloud/join.png)



## How to use ZConverter Cloud Migration

   1. **Click the target platform you want to migrate from "Cloud Migration" in the left menu.**
      
   ![menu](https://raw.githubusercontent.com/zconverter/ZCM-legacy/539f47f7e5e6e9534f9b31cd82f484af72df87ee/image/z-cloud/menu.png)

2. **Register on the source server.**
      
	* **ZConverter Cloud Source Agent installation.**

	* **You must register a source or target server for a migration operation, or install a zconverter cloud agent on the server for communication between the source or target server and the zconverter management server.**

	* **Download the Source Agent installation file corresponding to the source server's OS (Windows or Linux) from the "Download Agent" panel.**

	![menu](https://raw.githubusercontent.com/zconverter/ZCM-legacy/master/image/z-cloud/download_source_agent.png)
	
	1. **Windows Server**
			
		* **Remote access to the source server and copy the downloaded agent installation file to the source server.**

			![mst_win](https://raw.githubusercontent.com/zconverter/ZCM-legacy/master/image/z-cloud/mst_win.png)

		* **After running the installation file, select the installation language and click OK.**
		
			![select_lengage](https://raw.githubusercontent.com/zconverter/ZCM-legacy/master/image/z-cloud/select_lengage.png)

		* **Click "next"**
		
			![click_next](https://raw.githubusercontent.com/zconverter/ZCM-legacy/master/image/z-cloud/click_next.png)

		* **Click "I Agree"**
		
			![click_agree](https://raw.githubusercontent.com/zconverter/ZCM-legacy/master/image/z-cloud/click_agree.png)

		* **Click "Install"**
		
			![click_install](https://raw.githubusercontent.com/zconverter/ZCM-legacy/master/image/z-cloud/click_install.png)

		* **When the settings window appears, enter or select the following information.**
			* **Connect option : Choose "Public ZConverter SaaS(http://www.z-cloud.net)"**
			* **Agent mode : "Source"**
			* **User Information : Enter the account information you are currently accessing.**

				![setting](https://raw.githubusercontent.com/zconverter/ZCM-legacy/master/image/z-cloud/source_agent_setting.png)
			
	2. **Linux Server**

		* **SSH access to the source server, and copy the downloaded agent installation file to the /tmp directory of the source server.**

		* **Proceed with the installation through the following command.**

			![setting](https://raw.githubusercontent.com/zconverter/ZCM-legacy/master/image/z-cloud/linux_cmd.png)
			
			```script
			cd /tmp
			tar zxvf ZConverter_CloudSourceClient_Setup_RedHat_x86_V3.0_Build_3005.tar.gz
			cd zconverter_install_source
			```
			
		* **./install.sh command to proceed with the installation.**
			
		* **This is where the agent is to be installed. If you want to install it on a different path, enter that path. The default installation route is /ZConverteragent.**

			![setting](https://raw.githubusercontent.com/zconverter/ZCM-legacy/master/image/z-cloud/lin_install.sh.png)
			
		* **This is the type selection of ZConverter Cloud Migration.  
		
			If you use Public ZCM, choose Item 1, and if you use Private ZCM, select Item 2 and enter the IP of that ZCM.**
			
			![setting](https://raw.githubusercontent.com/zconverter/ZCM-legacy/master/image/z-cloud/lin_cmd_set1.png)
		
		* **This is the part where you enter the account of ZCM that you are currently using.**
			
			![setting](https://raw.githubusercontent.com/zconverter/ZCM-legacy/master/image/z-cloud/lin_cmd_set2.png)
		
		* **When the installation is complete as shown in the following screen, close the connection with the server and return to the z-cloud.net web portal.**
			
			![setting](https://raw.githubusercontent.com/zconverter/ZCM-legacy/master/image/z-cloud/lin_cmd_set3.png)
			
			![setting](https://raw.githubusercontent.com/zconverter/ZCM-legacy/master/image/z-cloud/lin_cmd_set4.png)
3. **Register a source server.**
	
	* **Click the "Load a server list" button to bring the server where the source agent is installed to the list.**
	
		![setting](https://raw.githubusercontent.com/zconverter/ZCM-legacy/master/image/z-cloud/register_a_source_server.png)
	
	* **Please check the connection status between the source server's agent and the ZConverter Cloud Management server through the leftmost icon in the server list. If the connection is disconnected, it is displayed as a red icon, and if the migration proceeds to this state, it may cause an error.**

		![setting](https://raw.githubusercontent.com/zconverter/ZCM-legacy/master/image/z-cloud/source_server_error.png)
	
	* **Click on the server to migrate, and select a source server imaging method in the "Create or select a source image" panel.**
		
		* **"Create a new image" option: Select if you create and migrate a new image of the server.**
		
		* **"Use an listing image" option: Select if you are migrating an existing server image.**
		
		![setting](https://raw.githubusercontent.com/zconverter/ZCM-legacy/master/image/z-cloud/register_a_source_server1.png)
		
		* **Check the disk to be migrated.**
		
		* **In the "Option" panel, select the type and path of the source image storage. 
		(The source image storage is used to store the image of the source server.)**
			* **"Basic" type: Local type storage that is created within the source server and stores images.**
				* We recommend creating a repository on a disk other than the disk to be migrated (when migrating Windows) or creating a repository in the root directory (when migrating Linux).
			* **"Advanced" type: Storage on a remote server. You can select a storage or other network storage within the target server.**
				* Select the "Target Repository" menu if you want to create a repository within the target server to store the source image.
		* **Click "next".**
		![setting](https://raw.githubusercontent.com/zconverter/ZCM-legacy/master/image/z-cloud/register_a_source_server2.png)


## Target VM generation


   1. **Log in to the Oracle Cloud site and access the user portal.**

      ![Login](https://raw.githubusercontent.com/zconverter/ZCM-legacy/master/image/login/login3.png)  

   2. **Enter the Custom Images menu.**

      ![Account User](https://raw.githubusercontent.com/zconverter/ZCM-legacy/master/image/legacy/custom_image_menu.png)  

   3. **Click Import image**
      ![Account Users](https://raw.githubusercontent.com/zconverter/ZCM-legacy/master/image/legacy/click_import_image.png)

   4. **Copy the address of the os version to be used below and retrieve the custom image.**
		``legacy-centos4-64bit : https://objectstorage.ap-seoul-1.oraclecloud.com/p/Lc9xSt8HrWT8FaLooqShd2_a2yK3ZCg-9ErbptAj8G9fcN-YnGWhFIK9ggdDjdvw/n/idffti7li8cs/b/oracle_vmdk_test_file/o/legacy-centos4-64bit``
 ![Api-Key](https://raw.githubusercontent.com/zconverter/ZCM-legacy/master/image/legacy/import_image_option.png)

   5. **After the image import, return to the instance menu and create an instance using the imported image.**
      ![Api-Key](https://raw.githubusercontent.com/zconverter/ZCM-legacy/master/image/legacy/custom_image_select.png)

		```script
		Access information : zconverter / Zcon@racle
		```
