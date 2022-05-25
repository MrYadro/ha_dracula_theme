# ha_dracula_theme
Home Assistant theme inspired by Dracula theme for VSCode

Installation:
1. Create a folder called themes in your root config folder
2. Open your configuration file, and add the following lines:
    frontend:
      themes: !include_dir_merge_named themes
3. Under the themes folder, copy and paste the dracula folder from this repo
4. In 'Developer Tools', select 'Services' and call the service 'frontend.reload_themes'
5. Select your profile, and under the theme dropdown, select Dracula!
6. If you wanted to set this as default for all users; create a new automation, access the yaml editor, and dump in the below:
```
    alias: Set Theme at Startup
    description: ''
    trigger:
      - event: start
        platform: homeassistant
    condition: []
    action:
      - data:
          name: Dracula
        service: frontend.set_theme
    mode: single
```

Screenshots:
![image](https://user-images.githubusercontent.com/6831087/170179638-4b23fa35-cbc5-47d6-a5a9-d87b0cf5376d.png)

![image](https://user-images.githubusercontent.com/6831087/170179661-5d15fbed-147d-4cb0-b079-b89f96c1f2b4.png)

![image](https://user-images.githubusercontent.com/6831087/170179675-0df40ecb-441a-460a-83df-9e0c36898a62.png)

![image](https://user-images.githubusercontent.com/6831087/170179689-0be7ff84-234f-4a77-8bcc-c5878e4b2197.png)
