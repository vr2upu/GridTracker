# GridTracker

Fix gt.js

 ... fix mainwindow mapFilter.data.label
 
 var g_gridViewArray = Array();
 
 ... fix mainwindow title display QSL count and QSO count
 
 var workline = ` - Worked ${g_viewInfo[g_currentOverlay][2]} Confirmed ${g_viewInfo[g_currentOverlay][3]}`
 

changed to

 ...
 
  if (g_appSettings.locale === "en")
 { var g_gridViewArray = Array();
 
 ... 
 
 var workline = ` - `+$.i18n("gt.TitleInfo.Worked")+` ${g_QSOcount} `+$.i18n("gt.TitleInfo.Confirmed")+` ${g_QSLcount}`
 
 ...
 
