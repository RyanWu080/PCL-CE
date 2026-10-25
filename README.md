**绠€浣撲腑鏂?* | [English](README-EN.md) | [绻侀珨涓枃](README-ZH_TW.md)

# PCL-CE unrestrict

璺熼殢 [PCL 绀惧尯鐗堬紙PCL-CE锛塢(https://github.com/PCL-Community/PCL-CE) 瀹樻柟鍙戠増锛岃嚜鍔ㄦ瀯寤鸿В闄ゅ湴鍖哄姛鑳介檺鍒剁殑鐗堟湰銆俓n
鏈粨搴撴槸涓汉缁存姢鐨勯潪瀹樻柟 fork锛屾簮鐮佸拰涓昏鍔熻兘鏉ヨ嚜涓婃父銆備慨鏀归泦涓湪 `RestrictedFeaturePolicy.cs`锛氫繚鐣欏湴鍖鸿瘎浼伴€昏緫锛岃鍦板尯鍔熻兘闄愬埗妫€鏌ョ洿鎺ユ斁琛屻€俓n
## 涓嬭浇

鍓嶅線 [Releases](https://github.com/RyanWu080/PCL-CE-unrestrict/releases)锛岄€夋嫨瀵瑰簲鐗堟湰鐨勯檮浠讹細

- 鏅€?Intel / AMD Windows 鐢佃剳锛歚PCL2_CE_Release_x64_unrestrict.exe`锛孊eta 瀵瑰簲 `PCL2_CE_Beta_x64_unrestrict.exe`銆俓n- Windows ARM 璁惧锛氶€夋嫨鏂囦欢鍚嶅寘鍚?`ARM64_unrestrict.exe` 鐨勯檮浠躲€俓n- 杩愯鐜锛歔.NET 10 Desktop Runtime](https://get.dot.net/10)銆俓n
璇蜂笅杞藉甫 `unrestrict` 鐨勫彲鎵ц闄勪欢銆俁elease 涓殑鑷姩婧愮爜鍘嬬缉鍖呮潵鑷畼鏂瑰師濮嬫爣绛撅紱瑙ｉ櫎闄愬埗琛ヤ竵淇濆瓨鍦ㄦ湰浠撳簱鐨?`.github/release-sync/RestrictedFeaturePolicy.cs`锛屾瀯寤烘潵婧愬拰鏂囦欢鏍￠獙鍊艰闄勪欢 `unrestrict-build.json`銆俓n
## 鑷姩鍙戝竷瑙勫垯

- 浠?**v2.15.1 姝ｅ紡鐗?*涓鸿捣鐐癸紱涓嶈ˉ鍙?v2.15.1 涔嬪墠鐨勭増鏈垨 v2.15.1 鐨勬棫 Beta銆俓n- 姣忓皬鏃剁 41 鍒嗛挓妫€鏌ュ畼鏂规柊 Release锛屽寘鎷悗缁洿楂樼増鏈殑姝ｅ紡鐗堝拰 Beta銆侴itHub 璋冨害鍙兘寤惰繜銆俓n- 鏍规嵁瀹樻柟瀵瑰簲鏍囩鍙栨簮鐮併€佸簲鐢ㄨˉ涓侊紝鍒嗗埆鏋勫缓 x64 鍜?ARM64锛涙瀯寤烘垚鍔熷悗鎵嶅叕寮€鍙戝竷銆俓n- 鏍囩銆佺増鏈爣棰樸€佽鏄庡拰姝ｅ紡 / Beta 鏍囪瘑璺熼殢瀹樻柟锛涢檮浠跺悕澧炲姞 `unrestrict`銆傚凡鍙戝竷鐗堟湰涓嶄細閲嶅鏋勫缓锛屽畼鏂硅鏄庢洿鏂版椂浼氬悓姝ャ€俓n- 涓婃父闄愬埗浠ｇ爜鍙樺寲銆佽ˉ涓佷笉鍏煎鎴栫紪璇戝け璐ユ椂鍋滄璇ョ増鏈彂甯冿紝绛夊緟妫€鏌ャ€俓n
Release 璇存槑鎸夊畼鏂瑰師鏂囧悓姝ワ紝鍏朵腑鐨勫閮ㄤ笅杞介摼鎺ュ拰绛惧悕淇℃伅灞炰簬瀹樻柟鍙戣鐗堬紱鏈粨搴撲慨鏀瑰悗鐨勯檮浠朵互鏈粨搴撶殑 Assets 涓哄噯銆俓n
## 鍒嗘敮涓庡伐浣滄祦

| 浣嶇疆 | 鐢ㄩ€?|
| --- | --- |
| `dev`锛堥粯璁ゅ垎鏀級 | 鏈粨搴撹鏄庛€佽嚜鍔ㄥ寲閰嶇疆鍜屽彂甯冭剼鏈?|
| `custom/dev-unrestricted` | 璺熼殢涓婃父 `dev` 鐨勫紑鍙戞簮鐮侊紝淇濈暀鍗曠嫭鐨勮В闄ら檺鍒舵彁浜わ紱鍏朵腑璇存槑鏂囨。娌跨敤涓婃父 |
| `sync-custom-dev.yml` | 姣忓皬鏃剁 23 鍒嗛挓鍚堝苟涓婃父寮€鍙戜唬鐮侊紝鍐茬獊鏃跺仠姝紝淇濈暀琛ヤ竵锛屼笉寮哄埗鎺ㄩ€?|
| `follow-official-releases.yml` | 妫€娴嬪畼鏂?Release銆佹瀯寤哄苟鍙戝竷瀵瑰簲鐨勮В闄ら檺鍒剁増 |

鍙戝竷鏋勫缓浣跨敤**瀹樻柟鐗堟湰鏍囩**锛屼笉浣跨敤寮€鍙戝垎鏀殑鏈€鏂颁唬鐮併€傚紑鍙戞簮鐮佸悓姝ヤ笌 Release 鍙戝竷鐩镐簰鐙珛銆俓n
## 褰撳墠楠岃瘉鑼冨洿

宸查獙璇佽嚜鍔ㄥ悓姝ャ€佺増鏈瓫閫夈€佺紪璇戝拰鍙戝竷娴佺▼锛涘疄闄呭惎鍔ㄣ€佺櫥褰曞拰涓嬭浇鍔熻兘浠嶉渶杩愯楠岃瘉銆傛瀯寤烘湭鍖呭惈瀹樻柟绉佹湁鏈嶅姟瀵嗛挜锛屼緷璧栬繖浜涘瘑閽ョ殑鏈嶅姟鍔熻兘鍙兘涓庡畼鏂规瀯寤轰笉鍚屻€傚畼鏂圭鍚嶄笉閫傜敤浜庝慨鏀瑰悗鐨勪簩杩涘埗鏂囦欢銆俓n
## 鏉ユ簮涓庤鍙痋n
- 涓婃父椤圭洰锛歔PCL-Community/PCL-CE](https://github.com/PCL-Community/PCL-CE)锛屽熀浜庨緳鑵剧尗璺冪殑 PCL 寮€婧愪唬鐮侊紝鐢辩ぞ鍖哄紑鍙戣€呯淮鎶ゃ€俓n- `Plain Craft Launcher 2/` 浣跨敤鍘熸湁 [鑷畾涔夎鍙瘉](Plain%20Craft%20Launcher%202/LICENCE)銆俓n- 鍏朵綑鐩綍浣跨敤 [Apache License 2.0](LICENSE)銆傚師鏈夎鍙瘉銆佺増鏉冨拰浣滆€呭綊灞炰繚鎸佷笉鍙樸€俓n
鏈?fork 鐨勮嚜鍔ㄥ寲鍜岃В闄ら檺鍒剁浉鍏抽棶棰樿鍏堝湪鏈粨搴撴帓鏌ワ紝鍕垮皢鍏跺綋浣滃畼鏂瑰彂琛岀増鍙嶉銆俓n