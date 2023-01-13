# GridTracker

Fix mainwindow title display QSL count and QSO count.


original gt.js

 ... 
 var g_gridViewArray = Array();
 ...
 var workline = ` - Worked ${g_viewInfo[g_currentOverlay][2]} Confirmed ${g_viewInfo[g_currentOverlay][3]}`

changed to

 ...
 var g_gridViewArray = Array();
 if (g_appSettings.locale === "en")
 {
 ... 
 var workline = ` - `+$.i18n("gt.TitleInfo.Worked")+` ${g_QSOcount} `+$.i18n("gt.TitleInfo.Confirmed")+` ${g_QSLcount}`
 ...
 
