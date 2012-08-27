# linux gae 配置

先配置两个文件，指定appid：

	/opt/google/goagent/server/python/app.yaml 
	/opt/google/goagent/server/proxy.ini

然后执行：

	python /opt/google/google_appengine/appcfg.py update  /opt/google/goagent/server/python
