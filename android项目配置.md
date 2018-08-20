#  Android 项目配置

## 常遇问题

​	报错信息：
Error:Execution failed for task ':app:preDebugAndroidTestBuild'.
> Conflict with dependency 'com.android.support:support-annotations' in project ':app'. Resolved versions for app (26.1.0) and test app (27.1.1) differ. See https://d.android.com/r/tools/test-apk-dependency-conflicts.html for details.

原因：external library中存在27.1.1版本的com.android.support:support-annotations或者其他未知原因
	
解决办法：
app下的build.gradle下的dependencies内添加					androidTestCompile('com.android.support:support-annotations:26.1.0') { force = true}





