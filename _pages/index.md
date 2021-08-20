---
layout: page
title: Index
---

### Hi, I'm Amy!

Lately I've been making some little mainframe-related web trinkets.
One of them is JCL syntax highlighting for highlight.js, because I might want to write stuff at some point and nothing seems to support syntax highlighting for mainframe languages.

<pre><code id='highlightedCode' class="language-jcl">//AFCPYCNT JOB CLASS=A,MSGCLASS=A,MSGLEVEL=(1,1),NOTIFY=&SYSUID
//*
//*---------------------------------------------
//* COPY PDS MEMBER AND COUNT NUMBER OF RECORDS
//*---------------------------------------------
//*
//CPYPCNT  EXEC PGM=ICETOOL
//CPYIN    DD DSN=USERNAME.SAMPLE.LIBRARY1(TESTFILE),DISP=SHR
//CPYOUT   DD DSN=USERNAME.SAMPLE.LIBRARY2(TESTFILE),
//            DISP=(NEW,CATLG,DELETE),
//            SPACE=(TRK,(1,1),RLSE),
//            DCB=(RECFM=FB,LRECL=80,BLKSIZE=800)
//CNTOUT   DD DSN=USERNAME.SAMPLE.ICEOUT(ICECOUNT),DISP=SHR
//TOOLIN   DD *
 COPY FROM(CPYIN) TO(CPYOUT) USING(CTL1)
 COUNT FROM(CPYIN) USING(CTL1) WRITE(CNTOUT) WIDTH(80) DIGITS(4)
/*
//CTL1CNTL DD *
 INCLUDE COND=ALL
/*
//TOOLMSG  DD SYSOUT=*
//DFSMSG   DD SYSOUT=*
/*
</code></pre>
