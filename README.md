# GridTracker

Fix mainwindow title display QSL count and QSO count
original gt.js
  var workline = ` - Worked ${g_viewInfo[g_currentOverlay][2]} Confirmed ${g_viewInfo[g_currentOverlay][3]}`

changed to
var workline = ` - `+$.i18n("gt.TitleInfo.Worked")+` ${g_QSOcount} `+$.i18n("gt.TitleInfo.Confirmed")+` ${g_QSLcount}`
