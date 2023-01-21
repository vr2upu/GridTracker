# Howto using , just download from GridTracker  https://gridtracker.org/  ,and install GridTracker.
  
  copy all files from here and replaced.

--------------------------------------

Fix gt.js

 ... fix mainwindow mapFilter.data.label
 
 var g_gridViewArray = Array();
 
changed to

 if (g_appSettings.locale === "en")
  
  {
  
  var g_gridViewArray = Array();
  
  ----------------------
 
 Fix mainwindow title display QSL count and QSO count
 
 var workline = ` - Worked ${g_viewInfo[g_currentOverlay][2]} Confirmed ${g_viewInfo[g_currentOverlay][3]}`
 

changed to
   
  var workline = ` - `+$.i18n("gt.TitleInfo.Worked")+` ${g_QSOcount} `+$.i18n("gt.TitleInfo.Confirmed")+` ${g_QSLcount}`
 
  -------------------------
 
Fix gt_roster.html

              <div>
                <label title="Only Decodes Containing...">
                  <input type="checkbox" id="onlyMsg" onchange="valuesChanged();" />
                  Only
                </label>
                
change to

              <div>
              <input type="checkbox" id="onlyMsg" onchange="valuesChanged();" />
                <label data-i18n="roster.secondary.exceptions.onlyMsg.label" title="Only Decodes Containing...">
                  Only
                </label>

--------------------------------------------


License Agreement and Copyright

GridTracker is Licensed under the BSD 3-Clause "New" or "Revised" License

The information contained within this site / document is subject to change without notice. The products identified within this document are not approval of or endorsements for any of the product names or trademarks appearing in this document.

Permission is granted to copy this site / information, at no charge for non-commercial purposes. The sources cited and present copyright notice is to be included in all copies. Recipients of copies are equally bound to abide by the present conditions. Prior written permission is required for any commercial use or publication of this document, in whole or in part.

Copyright ® 2022 GridTracker.org

All Rights Reserved Worldwide

WSJT-X is copyright ® Joseph Taylor, K1JT and the WSJT-X Development Group, et al.
https://physics.princeton.edu/pulsar/K1JT/wsjtx.html

JTDX is copyright ® Igor Chernikov, UA3DJY and Arvo Järve ES1JA
https://jtdx.tech/

HamClock is copyright ® Elwood Charles Downey, WB0OEW, Clear Sky Institute
https://www.clearskyinstitute.com/ham/HamClock/

Microsoft® is a registered trademark and Windows Vista®, Windows 7®, Windows 8®, Windows 8.1®, Windows 10® are trademarks of Microsoft Corporation.

Mac® and macOS® are registered trademarks of Apple, Inc.  

Linux® is the registered trademark of Linus Torvalds in the U.S. and other countries.

Linux AMD/Intel --
    AMD is a registered trademark of Advanced Micro Devices, Inc.
    Intel is a registered trademark of Intel Corporation

Linux ARM 32 / Raspberry PI - Odroid -- add registered trademark info/stuff
Raspberry Pi is a registered trademark of the Raspberry Pi Foundation

PSK-Reporter (are we using the .de or .info site for the GT feed?)

QRZ.Com:  Copyright 2021 by QRZ.com

ClubLog: Club Log © Michael Wells G7VJR

eQSL.cc: Copyright 1998-2021 Electronic QSL Card Centre, a division of Air Wave Productions, LLC

LotW : Copyright 2021 American Radio Relay League, Inc. All Rights Reserved

Log4OM   :  (Copyright 2011-2012) by Daniele Pistollato

N3FJP Loggers: (Copyright 1997-2021)Written by G. Scott Davis N3FJP
