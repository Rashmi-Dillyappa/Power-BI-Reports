# Power-BI-Reports
Career Gap Analysis Part 1 :DAX Code Used :

Failure Flag = IF('Career_Gap'[Job Offer] = "No", 1, 0);

Failure Percentage = 
DIVIDE(
    SUM('Career_Gap'[Failure Flag]), 
    COUNTROWS('Career_Gap')
) * 100 ;

Success Flag = IF('Career_Gap'[Job Offer] = "Yes", 1, 0);

Success Percentage = 
DIVIDE(
    SUM('Career_Gap'[Success Flag]), 
    COUNTROWS('Career_Gap')
) * 100 ;
