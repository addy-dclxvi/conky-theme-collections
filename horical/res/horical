#!/bin/bash
# a script to display a horizontal calendar on conky (hence the name horical :D)
# 
TODAY=`date +%d`
TOPLINE=" "
OVER=" "
REST=" "
# -------- This part is to find out the number of days in a month to display-----------#
a=`date +%-Y`
e1=`expr $a % 400`
e2=`expr $a % 100`
e3=`expr $a % 4`
if [ $e1 == 0 ]
  then c=1
  elif [ $e2 == 0 ]
  then c=0
  elif [ $e3 == 0 ] 
  then c=1
  else c=0
fi
p=`date +%-m`
# if the current year is not a leap one, c = 0
if [ $c == 0 ] 
  then
	if [ $p == 2 ]
	then b=28 # this is the number of days in Febuary 
	elif [ $p == 11 ] || [ $p == 4 ] || [ $p == 6 ] ||  [ $p == 9 ]
	then b=30
	else b=31
	fi
  else
	if [ $p == 2 ]
	then b=29 # the number of days in Febuary in a leap year
	elif [ $p == 11 ] || [ $p == 4 ] || [ $p == 6 ] ||  [ $p == 9 ]
	then b=30
	else b=31
	fi
fi
#--------------------- The bottom line which displays the days of month ----------#
i=1
if [ $TODAY -ne 1 ]
then
    while [ $i -lt $TODAY ]; do
        if [ $i -lt 10 ]
        then
            OVER="$OVER 0$i"
        else
            OVER="$OVER $i"
        fi
        i=$[$i+1]
    done
fi
i=$[$i+1]
if [ $TODAY -ne $b ]
then
    while [ $i -ne $[$b] ]; do
        if [ $i -lt 10 ]
        then
            REST="$REST 0$i"
        else
            REST="$REST $i"
        fi
        i=$[$i+1]
    done
    REST="$REST $b"
fi
#------------- the top line which displays the abbreviated weekday names-------#
k=`date +%u`
j=`date +%e`
f=`expr $j % 7`
if [ $k -lt $f ]
then 
	y=$[$k+8-$f]
else
	y=$[$k-$f+1]
fi
while [ $b -gt 0 ]; do
    case "$y" in
    1) TOPLINE="$TOPLINE Mo";;
    2) TOPLINE="$TOPLINE Tu";;
    3) TOPLINE="$TOPLINE We";;
    4) TOPLINE="$TOPLINE Th";;
    5) TOPLINE="$TOPLINE Fr";;
    6) TOPLINE="$TOPLINE Sa";;
    7) TOPLINE="$TOPLINE Su";;
    esac
    b=$[$b-1]
    y=$[$y+1]
    if [ $y -eq 8 ]
    then
        y=1
    fi
done
echo '${goto 180}''${font 'VCR OSD Mono:Regular:size=14'}'$TOPLINE | sed 's/Su/${color 383333}Su${color}/g' | sed 's/Su/${color fb0255}Su${color}/g'
echo ''
echo '${goto 180}''${font 'VCR OSD Mono:Regular:size=14'}''${color 7a7a7a}'$OVER '${color 23b3a7}'$TODAY'${color cacaca}'$REST
