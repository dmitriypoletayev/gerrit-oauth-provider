include_defs('//lib/maven.defs')
define_license('scribe')

gerrit_plugin(
  name = 'gerrit-oauth-provider',
  srcs = glob(['src/main/java/**/*.java']),
  resources = glob(['src/main/resources/**/*']),
  manifest_entries = [
    'Gerrit-PluginName: gerrit-oauth-provider',
    'Gerrit-HttpModule: com.googlesource.gerrit.plugins.oauth.HttpModule',
  ],
  provided_deps = ['//lib:gson'],
  deps = [':scribe-oauth'],
)

java_library(
  name = 'classpath',
  deps = [':gerrit-oauth-provider__plugin'],
)

maven_jar(
  name = 'scribe-oauth',
  id = 'org.scribe:scribe:1.3.7',
  sha1 = '583921bed46635d9f529ef5f14f7c9e83367bc6e',
  license = 'scribe',
  local_license = True,
)
