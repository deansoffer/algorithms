# algorithms

אלגוריתמים מושגים
גרף תשתית:  גרף תשתית של גרף מכוון הוא גרף לא מכוון אשר מכיל אותה קבוצת צמתים כמו הגרף המכוון, ומכיל את הקשתות בין זוגות הצמתים אשר היו ביניהם קשתות בגרף המקורי.
גרף העל = גרף רכיבי קשירות

# DFS\BFS חיפש המסלול הקצר ביותר לפי אורך מסלול

## DFS 
בדיקת קשירות (רקחים) 
מציאת המסלול הארוך ביותר בגרף
מציאת מעגלים
ליצור מבוכים
מציאת מסלולים מרובדים בגרפי זרימה

## BFS
O(V+E)
מציאת הנתיב הקצר ביותר בגרף (ללא משקלים) מקודקוד S לקודקודי הגרף
סריקת רוחב


# DAG (DIRECTED ACYCLIC GRAPH) 
למציאת המסלול הארוך ביותר, מכפילים כל קשת ב 1- ואז לאחר מציאת המסלול הקצר ביותר מכפילים שוב ב 1-


משפט - גרף לא מכוון הוא דו צדדי <----> בגרף אין מעגלים מאורך אי זוגי

מסלול אוילר הוא מסלול בגרף העובר בכל קשת בו בדיוק פעם אחת. 
מעגל אוילר הוא מסלול אוילר מעגלי (מתחיל ונגמר באותו צומת)

קוטר של גרף - המסלול הקצר ביותר הכי ארוך ביותר בין 2 קודקודים (כלומר אי אפשר לעשות כל מיני עיקופים מוזרים בגרף, קוטר חייב להיות מסלול קצר ביותר)



מסלולי קלים ביותר - אלגורתים פורד (הרעיון של האלגוריתם) \ בולצמן (מימוש האלגוריתם)
בלמן פורד - אסור מעגלים שליליים, יודע למצוא מעגלים שליליים . סיבוכיות VE. בשביל למצוא מעגל שלילי יש לעבור על הגרף V פעמים ואם יש שיפור בקודקוד שהתחלנו בו אז מצאנו מעגל שלילי. 
(כדי למצוא את כל המעגלים השליליים יש לעבור על הגרף N-1 פעמים)

# dijkstra
*דייקסטרה - למשקלים אי שליליים
O(ElogV)
חישוב הסמלול הקצר ביותר לפי משקל.
כל התקדמות לקחת את הקשת הקלה ביותר קודם.

פלויד ורשל  \ ג'ונסון - 2 אלגוריתמים עבור מק"בים בגרף מכוון עם משקלים שליליים - מטריצה מק"בים

*פלויד וורשל - מוצא מסלוליםם קצרים בין כל הקודקודים לכל הקודקודים בזמן O)V^3) - מותר משקלים שליליים (אסור מעגלים שליליים). פחות יעיל מגונסון במקרה הכללי
גונסון - חיבור קודקוד חדש S לכל הקודקודים בגרף המקורי, קשתות החיבור מS לשאר הקודקודים משקלם 0.


# עץ פורש מינימלי
מכיל את כל הקודקודים של הגרף , סכום משקלי הקשתות שלו הוא הכי קטן
*אלגוריתם קרוסקל - חלוקה כל קודקוד לקבוצה בודדת, לרוץ על הקשתות מהנמוך לגבוהה ולהתחיל לחבר קבוצות

*אלגוריתם פרים - לבחור קודקוד עם קבוצה ריקה של קשתות ובכל שלב מוסיפים את הקשת הקלה ביותר.

קרוסקל -  עפ"מ - מסמנים בכל שלב את הקשת הקלה ביותר שלא סוגרת מעגל, אם יש 2 קשתות הכי קלות באותו משקל, בוחרים אחת שרירותית
פרים - למציאת עפ"מ - בוחרים קבוצה ריקה ומוסיפים לרכיב הקשירות בכל פעם את הקשת והקודקוד הקלים ביותר בסביבתה, בכל שלב מסתכלים על הקשת הקלה ביותר שמחוברת לרכיב הקשירות.
סדרת משקלים שונים יוצרים עפ"מים שונים

פורד פלקרנסון - תרשימי זרימה (EF)O - צתמים וF זה הזרימה המקסימלית
MAX FLOW MIN CUT - גודל הזרימה המקסימלי כגודל החתך המינימלי

אדמונד קארפ - אלגוריתם זרימה למציאת הזרימה המקסימלית SOURCE -> SINK  
דומה לפורד פלרקנסון, רק שמשתמש בBFS
סיבוכיות: O)EV^2(

דיניק אלגוריתם (DINIC'S) - o(sqrt(v)E)
מפעילים BDF בכל שלב ליצרית גרף רמות שונות כאשר אנחנו מבטלים קשתות מלאות או מסלולים שהולכים אחורה, מחפשים מסלולים שונים על הגרף, מוצאים את הזרימה המינימלית על כל מסלול , מסיימים ברגע שאין יותר קיבול לאף מסלול

# רשתות 0-1
כל הקיבולים הם 1.

# דחיסת מידע
קוד הופמן ואלגוריתם חמדן
קוד הופמן חייב להיות עץ מלא 

