# Mozilla_DataCleaning
Data Cleaning Project for Mozilla

## Introduction
The historic data consists of 1% random samples from the deorphaned population
The 1% random sample is chosen independently every week .
We have 68 samples (see dates at the end) but we do not need to keep them all.
A dictionary for the fields can be found here: http://gecko.readthedocs.io/en/latest/toolkit/components/telemetry/healthreport/index.html

## Fields to Keep
thisPingDate,
lastPingDate,
geoCountry,
geckoAppInfo [
    vendor,
    name,
    version,
    platformBuildID,
    os,
    updateChannel],
data.last [
    org.mozilla.addons.gm-plugins,
        gmp-gmpopenh264,
        gmp-eme-adobe,
    org.mozilla.appInfo.appinfo,
        hotfixVersion,
        locale ],
    org.mozilla.profile.age [
        profileCreation ],
    org.mozilla.sysinfo.sysinfo [
       cpuCount,
       isWow64,
       memoryMB,
       architecture,
       name (os name),
       version (os version)],
data.days [
   date ],
      Org.mozilla.addons.counts,
plugin [
         theme,
         extension,
      org.mozilla.appInfo.appinfo [
         isDefaultBrowser  missing: ‘-1’],
      org.mozilla.appInfo.versions [
         appVersion,
         appBuildID ],
      org.mozilla.appSessions.previous [
         abortedActiveTicks missing: [],
         abortedTotalTime missing: [],
         cleanActiveTicks missing: [],
         cleanTotalTime missing: [] ],
      org.mozilla.searches.counts [
         _everything_ except “_v” ]
