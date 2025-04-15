# CBT874
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. 
Due to amazing work by Alison Zhang and Jake Choi repos are no longer deleted.

```
//***FILE 874 is from Sam Golob, and contains HELP members for      *   FILE 874
//*           many utilities on the CBT Tape which he, himself,     *   FILE 874
//*           finds useful.                                         *   FILE 874
//*                                                                 *   FILE 874
//*           Included is a member called $HEL, which is an XMIT    *   FILE 874
//*           of a load library containing the REVIEW TSO command   *   FILE 874
//*           from Greg Price (File 134, 135) whose aliases called  *   FILE 874
//*           HEL and FSH and FSHELP (full screen help) can be      *   FILE 874
//*           used to browse these members in full screen mode.     *   FILE 874
//*           (You can scroll inside them, up and down, even from   *   FILE 874
//*           TSO READY mode.)                                      *   FILE 874
//*                                                                 *   FILE 874
//*           Concatenate this file (the pds for CBT File 874)      *   FILE 874
//*           into the SYSHELP concatenation for your TSO session.  *   FILE 874
//*                                                                 *   FILE 874
//*           You can also use this file to decide which new tools  *   FILE 874
//*           from the CBT Tape that you might like to install and  *   FILE 874
//*           use for yourself.  The HELP members can show you      *   FILE 874
//*           what each tool does, and you might want to have that  *   FILE 874
//*           capability available if needed.                       *   FILE 874
//*                                                                 *   FILE 874
//*           When this pds is concatenated with your SYSHELP       *   FILE 874
//*           DD name, you can simply say HELP member, and you      *   FILE 874
//*           will get the help.  If the load modules for REVIEW,   *   FILE 874
//*           FSH, FSHELP, and HEL are installed, you can say       *   FILE 874
//*           (for example)   HEL member   or   FSH member          *   FILE 874
//*           and you will see the help member in full screen mode, *   FILE 874
//*           scrollable up and down.                               *   FILE 874
//*                                                                 *   FILE 874
//*           The ISPF statistics for each member of this pds       *   FILE 874
//*           will tell you which CBT Tape file, that program       *   FILE 874
//*           (described by the HELP member) came from.             *   FILE 874
//*                                                                 *   FILE 874
//*           email:   sbgolob@cbttape.org                          *   FILE 874
//*                                                                 *   FILE 874
//*        Some members of this PDS:                                *   FILE 874
//*                                                                 *   FILE 874
//*      NAME     VER.MOD     LAST MODIFIED    SIZE   ID            *   FILE 874
//*      ----     -------   -----------------  ----   --            *   FILE 874
//*      $$$#DATE  05.09  2025/01/23 13:43:31    12  CBT-509        *   FILE 874
//*      $$INDEX   01.13  2024/04/05  9:09:41    72  SBGOLOB        *   FILE 874
//*      $HEL      51.06  2025/01/16  7:54:21 23175  FILE134        *   FILE 874
//*      @FILE874  05.09  2025/01/23 13:43:20   127  CBT-509        *   FILE 874
//*      ABEND     05.00  1993/02/17 14:30:00  2307  FILE134        *   FILE 874
//*      ADDTO     01.00  2000/02/27 15:37:03    32  FILE452        *   FILE 874
//*      ADIS      01.02  2008/05/15  1:53:00    26  FILE185        *   FILE 874
//*      APFLIST   01.04  2019/06/02 11:46:13    44  FILE566        *   FILE 874
//*      BLKDISK   01.02  2012/07/26 14:31:04   334  FILE296        *   FILE 874
//*      BLKSPTRK  01.00  1999/05/06  8:32:34   195  FILE199        *   FILE 874
//*      BURN      01.02  2012/11/01 12:54:48    96  FILE878        *   FILE 874
//*      CATL      01.00  2000/02/27 15:37:05    36  FILE452        *   FILE 874
//*      CCAT      01.03  2019/01/27 17:41:47   129  FILE535        *   FILE 874
//*      CDSCB     01.00  2024/12/12 14:37:39    74  FILE300        *   FILE 874
//*      CINMX     01.05  2006/01/02 14:00:53    61  FILE731        *   FILE 874
//*      CNCLPG    01.10  2019/05/21  0:00:46   350  FILE826        *   FILE 874
//*      COPYFILE  01.17  2005/11/20 10:39:41   289  FILE229        *   FILE 874
//*      COPYMODS  00.87  2012/06/10 17:06:01   487  FILE229        *   FILE 874
//*      COUNT     01.02  2016/09/05 19:14:03    18  FILE300        *   FILE 874
//*      CPSCB     01.04  2020/06/22 10:08:29    52  FILE300        *   FILE 874
//*      CSCF      01.00  2024/12/12 21:03:42    63  FILE954        *   FILE 874
//*      DELINUSE  01.01  2024/08/21 13:30:18    61  FILE612        *   FILE 874
//*      DELNOENQ  01.02  1999/09/22  9:05:00   156  FILE411        *   FILE 874
//*      DSAT      01.00  2012/07/26 14:25:00   278  FILE296        *   FILE 874
//*      DSMF      01.00  2019/04/23 16:32:30    15  FILE300        *   FILE 874
//*      DSPACE    01.01  2003/05/27 10:49:00    36  FILE633        *   FILE 874
//*      DTEST     01.03  2019/04/24  2:23:43    38  FILE731        *   FILE 874
//*      DVAT      01.04  2019/04/24  2:39:21    35  FILE731        *   FILE 874
//*      DVOL      01.00  2003/06/29 10:24:39    56  FILE296        *   FILE 874
//*      EESCB     01.03  2006/01/02 14:03:11    24  FILE731        *   FILE 874
//*      FSH       ALIAS                                            *   FILE 874
//*      FSHELP    50.02  2021/12/18 21:02:43   939  FILE134        *   FILE 874
//*      HEL       ALIAS                                            *   FILE 874
//*      ICH       01.55  2010/01/16 16:46:10   327  FILE819        *   FILE 874
//*      IEBANTP   01.00  1989/04/12 11:59:00   238  FILE455        *   FILE 874
//*      IKJEEPTR  01.14  2022/10/02  9:04:43    78  FILE731        *   FILE 874
//*      INMXD     01.06  2019/04/24  9:17:48    46  FILE731        *   FILE 874
//*      JCLSET    01.01  2009/07/06 10:33:42    81  FILE452        *   FILE 874
//*      KMBAPFLB  01.00  2019/04/30 20:06:59    23  FILE566        *   FILE 874
//*      KONCAT    01.00  1998/05/22 13:15:00    44  FILE355        *   FILE 874
//*      LDS       01.00  2000/02/27 15:37:35    19  FILE452        *   FILE 874
//*      LISTHEAD  01.12  2024/03/05  0:41:34   120  FILE994        *   FILE 874
//*      LISTLPA   01.00  2024/08/05  0:07:33    38  FILE300        *   FILE 874
//*      LISTMOD   01.06  2025/01/21 14:25:24   148  FILE994        *   FILE 874
//*      LOADTEST  01.06  2019/06/20 11:14:50   250  FILE731        *   FILE 874
//*      LOCATE    01.12  2015/01/05 15:27:06    27  FILE612        *   FILE 874
//*      LOGOPTS   01.09  2016/05/02 11:49:35   110  FILE731        *   FILE 874
//*      LOOK      01.04  2022/10/02  9:39:31    38  FILE264        *   FILE 874
//*      LPSCB     01.04  2005/04/19 11:00:00    17  FILE300        *   FILE 874
//*      LWATMGR   01.00  2008/11/21 21:10:59    63  FILE797        *   FILE 874
//*      PDS86     86.17  2019/04/05 14:21:09 10078  FILE182        *   FILE 874
//*      PGLITE    01.01  2021/06/17 15:43:15   868  FILE182        *   FILE 874
//*      RELEASE   01.00  2007/04/04 23:20:14    23  FILE296        *   FILE 874
//*      REV       ALIAS                                            *   FILE 874
//*      REVED     ALIAS                                            *   FILE 874
//*      REVEDIT   51.05  2024/12/30 22:32:09  1972  FILE134        *   FILE 874
//*      REVIEW    51.04  2024/11/30  7:10:26  2311  FILE134        *   FILE 874
//*      REVLEV    50.02  2021/12/18 20:58:40   786  FILE134        *   FILE 874
//*      REVOUT    50.02  2021/12/18 20:59:13   473  FILE134        *   FILE 874
//*      REVPDS    50.02  2021/12/18 20:59:49   825  FILE134        *   FILE 874
//*      REVPDSE   50.02  2021/12/18 21:00:20   577  FILE134        *   FILE 874
//*      REVTSO    50.02  2021/12/18 21:00:47   330  FILE134        *   FILE 874
//*      REVUNIX   50.02  2021/12/18 21:01:13   596  FILE134        *   FILE 874
//*      REVVSAM   ALIAS                                            *   FILE 874
//*      RFE       50.02  2021/12/18 21:01:47   454  FILE134        *   FILE 874
//*      RGENR     01.02  2019/04/23 21:02:16    35  FILE836        *   FILE 874
//*      RPFHELP   01.71  2019/04/23 15:14:57   808  FILE415        *   FILE 874
//*      RXJCL     01.00  2007/03/15 15:34:06   348  FILE756        *   FILE 874
//*      SHOWTCAS  01.06  2021/06/18 14:36:23   101  FILE731        *   FILE 874
//*      SHOWTPVT  01.04  2021/06/18 12:31:38    23  FILE731        *   FILE 874
//*      STEPLIB   01.03  2016/05/02 11:35:45   118  FILE452        *   FILE 874
//*      TSUB      01.01  2019/04/24  9:40:26   368  FILE797        *   FILE 874
//*      TSUBQUIK  01.38  2019/04/24  9:52:30    27  FILE797        *   FILE 874
//*      TSUINFO   01.09  2025/01/23 13:28:55    58  FILE731        *   FILE 874
//*      TSVTTMO   01.05  2021/06/18 14:55:49    33  FILE731        *   FILE 874
//*      TSVT8     01.06  2024/07/17 13:15:02    47  FILE731        *   FILE 874
//*      UCBDASD   01.03  2019/05/20 21:35:25    43  FILE731        *   FILE 874
//*      UCBPRIV   01.06  2024/03/25  9:47:59    51  FIL1052        *   FILE 874
//*      UCBPUBL   01.07  2024/03/25  9:47:28    51  FIL1052        *   FILE 874
//*      UCBSTOR   01.04  2024/03/25  9:41:35    51  FIL1052        *   FILE 874
//*      UCBTAPE   01.06  2012/11/20 12:56:28    76  FILE731        *   FILE 874
//*      UKEYCSA   01.02  2021/06/18 14:33:31    31  FILE731        *   FILE 874
//*      ULUDASD   01.04  2019/05/20 21:33:29    46  FILE797        *   FILE 874
//*      ULUTAPE   01.07  2012/12/16 12:34:27    78  FILE873        *   FILE 874
//*      USERINFO  01.02  2012/08/01 13:44:03    59  FILE452        *   FILE 874
//*      VSAMANAL  00.88  2019/05/21  2:06:37   269  FILE294        *   FILE 874
//*      WHEREIS   01.00  2019/04/23 15:50:51    10  FILE836        *   FILE 874
//*      WHOSGOT   01.00  2000/02/27 15:37:00    17  FILE452        *   FILE 874
//*      WHOSON    01.00  2024/07/18  0:24:44    17  FILE314        *   FILE 874
//*      XEQ       01.00  2007/04/04 23:26:23    35  FILE296        *   FILE 874
//*                                                                 *   FILE 874
```
