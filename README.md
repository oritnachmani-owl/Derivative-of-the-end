<div dir="rtl">
לצורך צפייה בנתונים, בשאילתות ובדוחות, כאשר MS Access מותקן על המחשב האישי, יש להוריד למחשב את הקובץ End_Calculators_Signed.accdc.
&nbsp; 
לצורך צפייה בנתונים, בשאילתות ובדוחות, כאשר MS Access **אינו** מותקן על המחשב האישי, יש להוריד למחשב  את הקובץ End_Calculators_Runtime_Signed.accdc. בנוסף, יש להוריד את ה Runtime של MS Access 365 בקישור הבא:
https://support.microsoft.com/en-gb/office/download-and-install-microsoft-365-access-runtime-185c5a32-8ba9-491e-ac76-91cbe3ea09c9

&nbsp;


לאחר הורדת הקובץ המתאים ופתיחתו תתקבל הודעת אזהרה לגבי אופן חתימת הקובץ. יש לאשר את פתיחת הקובץ. לאחר מכן יש לבצע Unpack לקובץ לפי ההנחיות המופיעות במסך.

&nbsp;
 
**תאור ה Dataset ובנייתו**

ה Dataset שאיתו עבדתי נבנה, כאמור על בסיס ספרו של אבא הלל סילבר: A History of Messianic Speculation in Israel: from the first through the seventeenth centuries<sup>[\[1\]](#footnote-1)</sup>, פרקים III - VII והוא מורכב מהטבלאות הראשיות הבאות:

- טבלת מחש"קים - CalculatorsTbl
- טבלת חישובים - CalculationsTbl

מבנה הטבלאות הראשיות יפורט להלן.

בנוסף, בניתי שתי טבלאות עזר, האחת של ארצות והשנייה של אירועים היסטוריים מרכזיים:

- טבלת ארצות - CountriesTbl
- טבלת אירועים היסטוריים מרכזיים - MajorEventsTbl

תוכן כל הטבלאות מפורט בנספח א' להלן.

**טבלה 1 - מבנה טבלת המחש"קים: CalculatorsTbl**

| **שם השדה** | **תאור** |
| --- | --- |
| CalculatorId | מזהה המחש"ק - מפתח ראשי של הטבלה |
| Name | שם המחש"ק |
| Pages | עמודים בספרו של סילבר המתייחסים למחש"ק זה |
| CountryId | ארץ הפעולה הראשית |
| CityLocation | עיר או אזור במידה שידוע |
| Country2 | ארץ פעולה שנייה במידה שהייתה |
| Country3 | ארץ פעולה שלישית במידה שהייתה |
| Status | מעמד בקהילה, עיסוק |
| Mekubal | האם עסק בקבלה כן/לא |
| MainInfluence | משפיע עיקרי/מורה |
| Influence2 | משפיע נוסף |
| BirthYear | שנת לידה |
| YearOfDeath | שנת פטירה |
| CameToIsrael | עלה לארץ ישראל כן/לא |
| LocationInIsrael | מיקום בארץ ישראל |
| DeclaredAsMessiah | הכריז על עצמו או הוכרז כמשיח |
| Comments | הערות |
| EstimatedYearOfDeath | שנת מוות מוערכת |

**טבלה 2 - מבנה טבלת החישובים: CalculationsTbl**

| **שם השדה** | **תאור** |
| --- | --- |
| ID  | מזהה החישוב - מפתח ראשי של הטבלה |
| CalculatorId | מזהה המחש"ק - מפתח זר מטבלת המחש"קים |
| Type | סוג החישוב (0 חישוב בודד של מחש"ק, 1 חלק מסדרת חישובים של אותו מחש"ק, 2 חישוב ללא מחש"ק ידוע) |
| CalculationYear | שנת החישוב (במידה שידועה) |
| CalculatedEnd | שנת הקץ המחושב-שנה לועזית |
| HebrewYear | שנה עברית של הקץ המחושב |
| NatureOfEvent | אופי האירוע (ביאת המשיח, גאולה וכד') |
| MainSource | מקור ראשי לחישוב |
| MainSourceChapter | פרק במידה שמדובר במקור במקרא |
| SecandarySource | מקור משני לחישוב במידה שקיים |
| SecandarySourceChapter | פרק במקור המשני |
| ThirdSource | מקור שלישי במידה שקיים |
| Method | שיטת החישוב (גימטרייה, אסטרולוגיה וכד') |

לצורך מילוי הטבלאות הללו, ביצעתי, כאמור, קריאה רגילה, "קרובה" של הטקסט בפרקים הרלוונטיים בספרו של סילבר, דליתי מתוך הטקסט, מטא-דאטה של כל מחש"ק וחישוב רלוונטיים ועדכנתי אותם בטבלה המתאימה. יש לציין שלא כל המחש"קים המופיעים בפרקים הללו נכללו ב Dataset, משום שאין עבור כולם מספיק נתונים ביוגרפיים בספר. להלן דוגמה של מחש"ק שלא נכנס לרשימת המחש"קים ב Dataset משום שאין לגביו מספיק נתונים: "Zunz also quotes a manuscript in which Moses ben Judah (13 c.) announced 1260 as the Messianic year.".<sup><sup>[\[2\]](#footnote-2)</sup></sup> בדוגמה זו ניתן לראות כי עבור משה בן יהודה, לא מופיעים נתונים ביוגרפיים מהותיים כגון שנות חייו, מקום פעולתו וכד' ולכן בחרתי שלא להכניס אותו לרשימת המחש"קים.

**השלמת נתונים**

עבור מספר מחש"קים, לא קיימים בספרו של סילבר נתונים כגון שנת הלידה או שנת המוות. בשלב הראשון ניסיתי להשלים את הנתונים הללו מתוך מאגר המידע של Encyclopaedia Judaica.<sup>[\[3\]](#footnote-3)</sup> בשלב השני, עבור המקרים בהם לא היו נתונים גם במאגר זה בניתי את השדה \[EstimatedYearOfDeath\] בטבלת המחש"קים. בשדה זה הזנתי שנת מוות משוערת, לפי פרטים שכן מופיעים בספר של סילבר או ב Encyclopaedia Judaica, כגון, המאה או מחצית המאה בה פעל המחש"ק. בשלב האחרון, הוספתי בשאילתה CalculationsPlusCalculatorDataQry (מבנה השאילתה בנספח ב' להלן), שהיא שאילתה שמורכבת מפרטי חישובים ומחש"קים, עבור החישובים שהמחש"ק שלהם ידוע, שדה בשם: \[BirthYearCmb\] (תאור השדה בנספח ב' להלן). שדה זה מכיל את תאריך הלידה, במידה שהנתון קיים בטבלת המחש"קים, אם נתון זה לא קיים, השדה לוקח את תאריך המוות או את תאריך המוות המשוער, במקרה בו לא קיים תאריך מוות בטבלת המחש"קים ומפחית מהם שישים וחמש שנים. השתמשתי בנתון של שישים וחמש שנים כתוחלת חיים ממוצעת באופן שרירותי.

**תאור השאילתות**

להלן ריכוז השאילתות השונות בהן השתמשתי במסגרת העבודה. השאילתות מופיעות לפי סדר הפרקים בעבודה, בהם השתמשתי בהן.

**פרק ראשון - כלים ושיטות עבודה**

**שדה מחושב - \[BirthYearCmb\]** - שדה זה מכיל את תאריך הלידה, במידה שהנתון קיים בטבלת המחשבים, אם נתון זה לא קיים, השדה לוקח את תאריך המוות או את תאריך המוות המשוער, במקרה בו לא קיים תאריך מוות בטבלת המחשבים ומפחית מהם שישים וחמש שנים.

IIf(IsNull(\[CalculatorsTbl\]!\[BirthYear\]),

IIf(IsNull(\[CalculatorsTbl\]!\[YearOfDeath\]),\[CalculatorsTbl\]!\[EstimatedYearOfDeath\],\[CalculatorsTbl\]!\[YearOfDeath\])-65,

\[CalculatorsTbl\]!\[BirthYear\])

**פרק שני - שנות קץ שכיחות**

**שאילתה 1 - CalculatedEndInstancesQry** - השאילתה סופרת כמה מופעים קיימים עבור כל שנת קץ שחושבה.

SELECT

CalculationsTbl.CalculatedEnd,

Count(CalculationsTbl.ID) AS CountOfID

FROM

CalculationsTbl

GROUP BY

CalculationsTbl.CalculatedEnd

ORDER BY

Count(CalculationsTbl.ID) DESC;

**שאילתה 2 - RepeatedYearsQry** - השאילתה מוסיפה נתונים לגבי המחשבים (שם וארץ פעולה עיקרית) והחישובים (המקור העיקרי לחישוב) שחישבו את שנות הקץ השכיחות ביותר (מעל פעמיים).

SELECT

&nbsp;   CalculatedEndInstancesQry.CalculatedEnd,

&nbsp;   CalculatorsTbl.Name,

&nbsp;   CalculatedEndInstancesQry.CountOfID,

&nbsp;   CalculationsTbl.MainSource,

&nbsp;   CalculatorsTbl.CountryId

FROM

&nbsp;   (

&nbsp;       CalculatedEndInstancesQry

&nbsp;       INNER JOIN CalculationsTbl ON CalculatedEndInstancesQry.CalculatedEnd = CalculationsTbl.CalculatedEnd

&nbsp;   )

&nbsp;   LEFT JOIN CalculatorsTbl ON CalculationsTbl.CalculatorId = CalculatorsTbl.CalculatorId

WHERE

&nbsp;   (((CalculatedEndInstancesQry.CountOfID) > 2))

ORDER BY

&nbsp;   CalculatedEndInstancesQry.CountOfID DESC;

**פרק שלישי - מקורות החישוב**

**שאילתה 3 - MainSourcesQry** - השאילתה מונה כמה פעמים מופיע כל מקור ראשי בטבלת החישובים וממיינת את התוצאות בסדר יורד, כלומר מהמקור השכיח ביותר לנדיר ביותר.

SELECT

&nbsp;   Count(CalculationsTbl.ID) AS CountOfID,

&nbsp;   CalculationsTbl.MainSource

FROM

&nbsp;   CalculationsTbl

GROUP BY

&nbsp;   CalculationsTbl.MainSource

ORDER BY

&nbsp;   Count(CalculationsTbl.ID) DESC;

**שאילתה 4 - MainSourcesWithoutNAQry** - סינון החישובים שמקורם אינו ידוע על פי סילבר מתוצאות שאילתת המקורות.

SELECT

&nbsp;   Count(CalculationsTbl.ID) AS CountOfID,

&nbsp;   CalculationsTbl.MainSource

FROM

&nbsp;   CalculationsTbl

GROUP BY

&nbsp;   CalculationsTbl.MainSource

HAVING

&nbsp;   (((CalculationsTbl.MainSource) <> "N/A"))

ORDER BY

&nbsp;   Count(CalculationsTbl.ID) DESC;

**פרק רביעי - חישוב בימי חייו של המחש"ק**

**שאילתה 5 -** CalculationsPlusCalculatorDataQry - מכילה אוסף של שדות משתי הטבלאות הראשיות לגבי חישובים שיש להם מחשב בלבד, כלומר, בשאילתה זו מופיעים נתונים לגבי 51 חישובים של 40 מחשבים (יש כאמור מחשבים שביצעו מספר חישובים שונים).

**שדה מחושב - InCalculatorLifetime** - השדה נמצא בתוך השאילתה CalculationsPlusCalculatorDataQry הנ"ל השדה בודק האם שנת הלידה של המחשב+שישים וחמש < שנת הקץ שחושבה.

InCalculatorLifetime: \[CalculatorsTbl\]!\[BirthYear\]+65>\[CalculationsTbl\]!\[CalculatedEnd\]

**שאילתה 6 - InCalculatorLifetimeQry** השאילתה מחלקת את המחשבים לשלוש קבוצות: מחשבים שחישבו בתקופת חייהם, מחשבים שחישבו לאחר מותם וכאלה שאין לנו מידע לגביהם וזאת לפי הערך של השדה המחושב InCalculatorLifetime.

SELECT

&nbsp;   CalculationsPlusCalculatorDataQry.InCalculatorLifetime,

&nbsp;   Count(CalculationsPlusCalculatorDataQry.ID) AS CountOfID,

&nbsp;   IIf(

&nbsp;       IsNull(\[InCalculatorLifetime\]),

&nbsp;       "לא ידוע",

&nbsp;       IIf(

&nbsp;           \[InCalculatorLifetime\],

&nbsp;           "בתקופת החיים",

&nbsp;           "לאחר המוות"

&nbsp;       )

&nbsp;   ) AS Label

FROM

&nbsp;   CalculationsPlusCalculatorDataQry

GROUP BY

&nbsp;   CalculationsPlusCalculatorDataQry.InCalculatorLifetime,

&nbsp;   IIf(

&nbsp;       IsNull(\[InCalculatorLifetime\]),

&nbsp;       "לא ידוע",

&nbsp;       IIf(

&nbsp;           \[InCalculatorLifetime\],

&nbsp;           "בתקופת החיים",

&nbsp;           "לאחר המוות"

**פרק חמישי - פיזור גיאוגרפי**

**שאילתה 7 - CalculatorsCountriesQry** השאילתה בנויה על בסיס טבלת המחשבים, מקבצת את הארצות הראשיות בהן פעלו המחשבים ומונה אותן.

SELECT

&nbsp;   Count(CalculatorsTbl.CalculatorId) AS CountOfCalculatorId,

&nbsp;   CountriesTbl.CountryName,

&nbsp;   CountriesTbl.CountryId

FROM

&nbsp;   CountriesTbl

&nbsp;   RIGHT JOIN CalculatorsTbl ON CountriesTbl.CountryId = CalculatorsTbl.CountryId

GROUP BY

&nbsp;   CountriesTbl.CountryName,

&nbsp;   CountriesTbl.CountryId

ORDER BY

&nbsp;   Count(CalculatorsTbl.CalculatorId) DESC;

**שדה מחושב - CalculationYearCmb** - מכיל את תאריך החישוב הידוע או המשוער. כלומר, במידה שתאריך החישוב צוין בספרו של סילבר, הוא נרשם בשדה זה. במידה שהתאריך אינו ידוע, נלקחה שנת הלידה של המחשב (במידה שהיא ידועה) והתווספו לה שלושים שנים.

IIf(IsNull(\[CalculationsTbl\]!\[CalculationYear\]),\[CalculatorsTbl\]!\[BirthYear\]+30,\[CalculationsTbl\]!\[CalculationYear\])

**פרק שישי - שנות חישוב מול אירועים היסטוריים**

**שאילתה 8 - CalculationsAndMajorEventsQry** השאילתה מחברת בין רשימת האירועים ההיסטוריים לבין רשימת החישובים שיש להם מחשב ידוע ומוצאת איזה חישובים בוצעו בין תחילת אירוע היסטורי מסוים לבין 25 שנים לאחר סיומו.

SELECT

&nbsp;   CalculationsPlusCalculatorDataQry.ID,

&nbsp;   MajorEventsTbl.ID,

&nbsp;   MajorEventsTbl.EventName,

&nbsp;   CalculationsPlusCalculatorDataQry.CalculationYearCmb

FROM

&nbsp;   MajorEventsTbl

&nbsp;   INNER JOIN CalculationsPlusCalculatorDataQry ON CalculationsPlusCalculatorDataQry.CalculationYearCmb >= MajorEventsTbl.EventStartYear

&nbsp;   AND CalculationsPlusCalculatorDataQry.CalculationYearCmb <= MajorEventsTbl.EventEndYear + 25

- Abba Hillel Silver, A History of Messianic Speculation in Israel: from the first through the seventeenth centuries. New York, 1927. [↑](#footnote-ref-1)

- Abba Hillel Silver, A History of Messianic Speculation in Israel: from the first through the seventeenth centuries. New York, 1927, p.99. [↑](#footnote-ref-2)

- <https://go-gale-com.elib.openu.ac.il/ps/i.do?p=GVRL&u=openuni&id=GALE%7C5GVQ&v=2.1&it=etoc>. Accessed 1 August 2025. [↑](#footnote-ref-3)
