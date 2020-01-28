# RAFAEL Challenge - DataHack 2017 



# DataHack has ended!

**Thanks to all the participants! Final scoreboard and solutions can be found under the `solutions` folder.**

**If you wish to upload a solution, please use "pull request" or send it to RocketDataScientist@gmail.com**




# DATA IS ONLINE!
## Two options to get the data:

**Option (1) Send a mail to RocketDataScientist@gmail.com with the folowing details:**

* Group name
* Team leader name + mobile number (for whatsapp group notifications)
* Group participants names

**Option (2) Come to the Rafael booth with your laptop between 18:00-19:30**


![It takes a rocket data scientist!](https://github.com/DataHackIL/RocketDataScientist/blob/master/logo.jpg "It takes a rocket data scientist!")

<div dir="rtl">

באתגר המצורף עליכם לזהות את סוג הרקטה מתוך מקטע מעוף שלה. 
הסט בנוי ממקטעי מסלולים באורכים 5-15 שניות , שתי מדידות בשניה.
שימו לב! בסט האימון יש 25 סוגי מטרות אבל **בסט הבחינה יש יותר**. מטרות שלא הופיעו בסט האימון יש לתייג כסוג 26

**לזוכים מצפה פרס מדליק - פירוט בהמשך העמוד**

**ניתן לשאול אותנו שאלה באמצעות פתיחת issue**

**מוזמנים להעלות פונקציות עזר לתיקיית community scripts. קוד המועלה לתיקייה זו מצורף As Is והשימוש בו על אחריותכם**

## בתיקייה המצורפת תמצאו את הקבצים הבאים:

* train.csv - סט האימון
* test.csv - סט הבחינה
* Submission_sample - דוגמת הגשה
* readAndSubmit_sample.py - קובץ פייתון לדוגמא לקריאת הדאטה והכנת קובץ ההגשה
* readAndSubmit_sample.ipynb - קובץ פייתון nb לדוגמא לקריאת הדאטה והכנת קובץ ההגשה
* readAndSubmit_sample.m - קובץ מטלאב לדוגמא לקריאת הדאטה והכנת קובץ ההגשה
* csv2kml.py - קובץ פייתון לדוגמא המייצר מתוך דאטה חלקי קובץ ויזואליזציה עבור Google Earth
* csv2kml.m - קובץ מטלאב לדוגמא המייצר מתוך דאטה חלקי קובץ ויזואליזציה עבור Google Earth
* Picture1.png - דוגמא לויזואליזציה שנוצרה באמצעות הקבצים הנ"ל

**שימו לב: קבצי הפייתון נבדקו בסביבת פייתון 2.7. קבצי המטלאב נבדקו בגרסא 2014a**

# חוקי האתגר:

* על קובץ ההגשה להיות באותו פורמט כמו בדוגמה המצורפת
* ניתן להגיש עד 3 הגשות במהלך ההאקתון.
  * להגשה יש לשלוח את קובץ ההגשה למייל RocketDataScientist@gmail.com
  * בכותרת יש לכתוב submission: TeamName. במקום TeamName יש לרשום את שם הקבוצה.
* הגשה אחרונה תינתן עד יום שישי 27/10, שעה 9:00. לאחר מכן לא תתקבלנה הגשות.
* תוצאות ביניים להגשות תתקבלנה במייל חוזר בהקדם האפשרי (בכל זמן שנציג החברה יהיה בהאקתון) עד יום חמישי 26/10 בשעה 21:00
* ציון סט הבחינה יחושב ע"י ה f1-score הממוצע, כאשר הקבוצה עם הציון הגבוה ביותר היא המנצחת.

## שימו לב!
**בכל הגשה שתשלחו, תקבלו בחזרה את ציון סט הבחינה ששלחתם, ובנוסף תמונה של ה confusion matrix שהתקבלה.**


# פרסים לזוכים:
**המנצחים באתגר יזכו בכונן SSD חיצוני קומפקטי נייד בנפח 525GB מסוג [Glyph Atom SSD](https://www.cnet.com/products/glyph-atom-ssd/review/). השותף המושלם לאימון רשתות עמוקות on-the-go, ולגיבוי סופר-מהיר של קבצים**

<img src="https://www.nettbee.com/Uploads/images/Nuevos/SKU473375-3.jpeg" alt="Glyph Atom SSD 525GB" height="300" width="450" border="2" align="center" > 

# מידע על בסיס הנתונים:

* 300,000 מקטעי מסלולים, בין 5 ל 15 שניות, עם תדר דגימה של 2 הרץ (דגימה כל חצי שנייה).
בכל דגימה נתוני מיקום XYZ ומהירות XYZ מורעשים.
* כל מקטעי המסלולים מיושרים לכיוון המהירות ההתחלתית ומתחילים מ X=0, Y=0 ובגובה האמיתי. הכיוון החיובי של ציר Z הוא כלפי מעלה, כלומר VelZ חיובי מציין מטרה בעלייה
* סט האימון הינו כ-10% מתוך בסיס הנתונים ומכיל מסלולים מתויגים ל 25 סוגים.
* סט הבחינה הינו כ 90% מתוך בסיס הנתונים ואותו נדרש לסווג ל 26 מסלולים - הכוונה ל 25 המסלולים מסט האימון וסיווג מספר 26 לכל מסלול אשר מתקבלת עבורו החלטה שלא לסווגו לאף אחד מ 25 המסלולים 


* ויזואליזצייה לדוגמה עבור מספר מקטעי מסלולים של אחת המטרות. בכחול מסלולים בעלייה ובאדום מסלולים בירידה:

</div>

![visualization](/visualiztion/Picture1.png)


