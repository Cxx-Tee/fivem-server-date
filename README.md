## ขั้นตอนติดตั้งสคริปต์ 
วิธีแรกให้หาสคริปต๋หรือสคริปต์ของท่านมาให้พร้อม เริ่ม
1.วิธีแรกให้นำสคริปของท่านเองมาว่างFile ของท่านเอง หรือสร้าง File ตัวอย่าง
```
C:/Server/server-data/resources/resources/[base]/test_script
```
2.ให้ค้ดลอกชื่อสคริปต์ของท่านมาวางไว้ใน server.cfg 
[ตัวอย่างที่1](https://docs.fivem.net/docs/server-manual/server-commands/) 
[ตัวอย่างที่2](https://docs.fivem.net/docs/server-manual/setting-up-a-server-vanilla/)
[ตัวอย่างที่3](https://cdn.discordapp.com/attachments/894242984600686663/1118925115963478156/image.png)
```
## [base] ## File ชื่อโฟล์ของท่านเองที่สร้างขึ้น
ensure test_script
start test_script

ensure [base]
start [base]
```

## EN 33 ##
Script installation steps

# cfx-server-data
_The data repository for Cfx.re servers_

## Deprecation notice
This repository itself is considered finalized/immutable and is currently archived. Pull requests or issue reports were not merged for a *while*, using the contents of the repository should still be fine (and this shouldn't change until mentioned otherwise).

In the future, relevant parts of this repository will be moved to [citizenfx/fivem](https://github.com/citizenfx/fivem) to be bundled with actual server builds, and the examples (+ legacy API-like resources) will be moved to a new repository.

If there's any critical issue in the code in this repository, posting on the [Cfx.re forums](https://forum.cfx.re/) may work.

## Usage
1. Make sure to `git clone`. Don't "Download ZIP", as that'll make it _much_ harder to update to newer versions.
2. Put custom resources in `resources/[local]/` if you don't want to be affected by any random messups.

### Advanced usage
You can also consider using the repository as a submodule + symlink for your own Git repository:

**Linux**:
```
$ git submodule add https://github.com/citizenfx/cfx-server-data.git vendor/server-data
$ ln -s ../vendor/server-data/resources/ 'resources/[base]/'
```

**Windows**:
```
> git submodule add https://github.com/citizenfx/cfx-server-data.git vendor/server-data
> mklink /d resources\[base] ..\vendor\server-data\resources
```

## Policy
You can make pull requests to propose changes that benefit _everyone_. Add new useful resources, change/improve
existing ones - anything goes, as long as you make sure to:

1. Not break existing users/APIs.
2. Not change default behavior without a toggle.
3. Use best practices (convars over config files, native commands wherever possible, etc.)

Modifying or rewriting existing resources in this repository for local use only is _strongly_ discouraged.
| Version | Supported          |    
| ------- | ------------------ |
| 0.5.x   | :white_check_mark: |      
| 0.0.3.x   | :x:                |      
| 4.0.x   | :white_check_mark: |      
| < 4.0   | :x:                |    
