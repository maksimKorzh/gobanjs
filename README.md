# Goban JS
Simple Go Board to embed into websites

# Example usage
Assuming you have downloaded file **goban.js** and
hosting it along with an HTML page where you want to
embed a Go board
<hr>
```html
  <!-- SIMPLE GOBAN -->
  <div id="goban"></div>
  <script src="goban.js"></script>
  <script>
    const goban = new Goban({
      'size': 19,
      'width': 800,
    });
  </script>
```
<a href="https://maksimkorzh.github.io/gobanjs/simple_goban.html">see example...</a>

```html
  <!-- SGF GAME VIEWER -->
  <div id="goban"></div>
  <div style="display: flex;">
    <button onclick="goban.firstMove()" style="width: 115px; font-size: 30px;"><<<</button>
    <button onclick="goban.prevFewMoves(5)" style="width: 115px; font-size: 30px;"><<</button>
    <button onclick="goban.prevMove()" style="width: 115px; font-size: 30px;"><</button>
    <button onclick="goban.nextMove()" style="width: 115px; font-size: 30px;">></button>
    <button onclick="goban.nextFewMoves(5)" style="width: 115px; font-size: 30px;">>></button>
    <button onclick="goban.lastMove()" style="width: 115px; font-size: 30px;">>>></button>
  </div>
  <script src="goban.js"></script>
  <script>
    const sgf = `
      (;GM[1]FF[4]CA[UTF-8]AP[CGoban:3]ST[2]
      RU[Japanese]SZ[19]KM[6.50]TM[1200]OT[5x60 byo-yomi]
      PW[dlzgo]PB[cmkgo]BR[6k]DT[2024-08-30]PC[The KGS Go Server at http://www.gokgs.com/]RE[B+1.50]
      ;B[qd]BL[1188.217] ;W[dd]WL[1196.063] ;B[pq]BL[1174.313] ;W[od]WL[1186.545] ;B[oc]BL[1166.035] ;W[nc]WL[1183.298]
      ;B[pc]BL[1163.779] ;W[nd]WL[1181.717] ;B[jd]BL[1161.858] ;W[qe]WL[1178.822] ;B[re]BL[1159.476] ;W[rf]WL[1160.205]
      ;B[pe]BL[1156.124] ;W[qf]WL[1158.325] ;B[pd]BL[1148.459] ;W[rd]WL[1155.346] ;B[rc]BL[1146.643] ;W[se]WL[1153.026]
      ;B[nf]BL[1143.424] ;W[kc]WL[1107.672] ;B[jc]BL[1139.698] ;W[kd]WL[1099.427] ;B[ke]BL[1136.755] ;W[le]WL[1098.123]
      ;B[ld]BL[1132.259] ;W[lc]WL[1076.159] ;B[lf]BL[1129.903] ;W[me]WL[1069.679] ;B[mf]BL[1127.23] ;W[jb]WL[1051.366]
      ;B[ib]BL[1120.452] ;W[kb]WL[1049.739] ;B[je]BL[1112.975] ;W[nb]WL[1017.121] ;B[mb]BL[1108.031] ;W[ne]WL[988.291]
      ;B[ob]BL[1101.277] ;W[oa]WL[971.977] ;B[pa]BL[1098.286] ;W[na]WL[970.144] ;B[cc]BL[1077.228] ;W[cd]WL[965.409]
      ;B[dc]BL[1075.519] ;W[ed]WL[962.378] ;B[fb]BL[1073.158] ;W[fc]WL[952.169] ;B[gb]BL[1067.375] ;W[bc]WL[935.175]
      ;B[ec]BL[1064.761] ;W[cb]WL[921.877] ;B[fd]BL[1060.838] ;W[di]WL[908.631] ;B[db]BL[1056.363] ;W[da]WL[903.141]
      ;B[gc]BL[1051.761] ;W[bb]WL[876.294] ;B[dg]BL[1046.317] ;W[cf]WL[862.665] ;B[ef]BL[1042.643] ;W[cg]WL[853.583]
      ;B[ei]BL[1032.91] ;W[ej]WL[824.619] ;B[dj]BL[1025.47] ;W[eh]WL[816.404] ;B[fi]BL[1023.31] ;W[dh]WL[813.083]
      ;B[dk]BL[1012.84] ;W[fh]WL[803.002] ;B[fj]BL[1010.517] ;W[fe]WL[786.407] ;B[dp]BL[1004.586] ;W[fq]WL[779.061]
      ;B[eq]BL[1001.572] ;W[fp]WL[774.765] ;B[cn]BL[998.417] ;W[jp]WL[771.754] ;B[lq]BL[996.038] ;W[ek]WL[752.318]
      ;B[el]BL[991.628] ;W[fk]WL[750.81] ;B[gk]BL[974.005] ;W[fl]WL[748.447] ;B[gl]BL[968.39] ;W[fm]WL[746.235]
      ;B[hj]BL[963.427] ;W[gm]WL[723.376] ;B[em]BL[959.508] ;W[hi]WL[647.266] ;B[il]BL[926.608] ;W[en]WL[620.559]
      ;B[dn]BL[922.178] ;W[im]WL[602.966] ;B[fn]BL[919.052] ;W[gn]WL[600.237] ;B[eo]BL[916.988] ;W[jl]WL[597.077]
      ;B[qi]BL[913.258] ;W[rh]WL[589.612] ;B[ri]BL[911.382] ;W[pf]WL[551.056] ;B[qb]BL[907.866] ;W[po]WL[549.816]
      ;B[qo]BL[905.36] ;W[qn]WL[543.85] ;B[qp]BL[903.026] ;W[pn]WL[541.833] ;B[rm]BL[901.804] ;W[rn]WL[528.669]
      ;B[ql]BL[896.696] ;W[oq]WL[525.635] ;B[or]BL[894.255] ;W[nq]WL[516.594] ;B[nr]BL[892.691] ;W[mq]WL[512.828]
      ;B[mr]BL[890.748] ;W[pp]WL[501.995] ;B[qr]BL[888.742] ;W[lp]WL[501.224] ;B[kq]BL[886.519] ;W[kp]WL[495.818]
      ;B[mm]BL[881.599] ;W[ij]WL[484.954] ;B[no]BL[876.136] ;W[np]WL[478.178] ;B[ol]BL[874.44] ;W[kf]WL[453.364]
      ;B[kg]BL[867.971] ;W[jf]WL[451.734] ;B[if]BL[864.555] ;W[jg]WL[450.495] ;B[jh]BL[862.909] ;W[ig]WL[449.196]
      ;B[hg]BL[859.738] ;W[ih]WL[447.927] ;B[kh]BL[857.582] ;W[ie]WL[441.623] ;B[id]BL[855.101] ;W[hf]WL[425.823]
      ;B[he]BL[853.153] ;W[if]WL[362.579] ;B[ge]BL[847.852] ;W[gf]WL[338.038] ;B[hc]BL[845.705] ;W[mh]WL[300.155]
      ;B[oh]BL[841.896] ;W[og]WL[227.87] ;B[mi]BL[823.71] ;W[nh]WL[113.224] ;B[ni]BL[817.168] ;W[ng]WL[48.27]
      ;B[li]BL[810.461] ;W[ll]WL[60]OW[5] ;B[ml]BL[801.456] ;W[lm]WL[60]OW[5] ;B[jq]BL[794.518] ;W[iq]WL[60]OW[5]
      ;B[ir]BL[792.346] ;W[hr]WL[60]OW[5] ;B[jr]BL[790.41] ;W[ip]WL[60]OW[5] ;B[ci]BL[783.81] ;W[ch]WL[60]OW[5]
      ;B[bi]BL[782.156] ;W[bh]WL[60]OW[5] ;B[bj]BL[780.115] ;W[rq]WL[60]OW[5] ;B[qq]BL[775.485] ;W[fr]WL[60]OW[5]
      ;B[er]BL[769.131] ;W[es]WL[60]OW[5] ;B[ds]BL[766.844] ;W[fs]WL[60]OW[5] ;B[cr]BL[765.549] ;W[ro]WL[60]OW[5]
      ;B[lg]BL[761.475] ;W[ph]WL[60]OW[5] ;B[oi]BL[758.373] ;W[qh]WL[60]OW[5] ;B[pi]BL[756.706] ;W[si]WL[60]OW[5]
      ;B[sj]BL[754.832] ;W[sh]WL[60]OW[5] ;B[rk]BL[753.299] ;W[fo]WL[60]OW[5] ;B[lk]BL[739.444] ;W[kk]WL[60]OW[5]
      ;B[kj]BL[735.632] ;W[jj]WL[60]OW[5] ;B[ji]BL[732.634] ;W[mn]WL[60]OW[5] ;B[nn]BL[730.153] ;W[mo]WL[60]OW[5]
      ;B[om]BL[728.616] ;W[en]WL[60]OW[5] ;B[ep]BL[725.482] ;W[dl]WL[60]OW[5] ;B[cl]BL[722.996] ;W[dm]WL[60]OW[5]
      ;B[cm]BL[721.646] ;W[ai]WL[60]OW[5] ;B[ck]BL[719.081] ;W[rp]WL[60]OW[5] ;B[rr]BL[714.278] ;W[sr]WL[60]OW[5]
      ;B[rs]BL[711.651] ;W[sm]WL[60]OW[5] ;B[sl]BL[709.546] ;W[sn]WL[60]OW[5] ;B[sc]BL[706.255] ;W[qm]WL[60]OW[5]
      ;B[rl]BL[699.846] ;W[oo]WL[60]OW[5] ;B[sd]BL[696.107] ;W[re]WL[60]OW[5] ;B[of]BL[692.168] ;W[pg]WL[60]OW[5]
      ;B[ii]BL[664.574] ;W[gg]WL[60]OW[5] ;B[ja]BL[623.803] ;W[ka]WL[60]OW[5] ;B[mc]BL[615.212] ;W[md]WL[60]OW[5]
      ;B[oe]BL[603.72] ;W[ma]WL[60]OW[5] ;B[ia]BL[599.575] ;W[on]WL[60]OW[5] ;B[nm]BL[596.35] ;W[pm]WL[60]OW[5]
      ;B[pl]BL[594.554] ;W[is]WL[60]OW[5] ;B[lr]BL[589.637] ;W[js]WL[60]OW[5] ;B[ks]BL[587.084] ;W[hs]WL[60]OW[5]
      ;B[ik]BL[546.315] ;W[gi]WL[60]OW[5] ;B[jk]BL[542.309] ;W[gj]WL[60]OW[5] ;B[jm]BL[536.458] ;W[jn]WL[60]OW[5]
      ;B[kl]BL[534.525] ;W[kn]WL[60]OW[5] ;B[km]BL[532.688] ;W[ln]WL[60]OW[5] ;B[hm]BL[530.187] ;W[in]WL[60]OW[5]
      ;B[ea]BL[511.727] ;W[ca]WL[60]OW[5] ;B[aj]BL[504.094] ;W[ah]WL[60]OW[5] ;B[hn]BL[483.622] ;W[ho]WL[60]OW[5]
      ;B[hl]BL[482.303] ;W[sq]WL[60]OW[5] ;B[ss]BL[464.82] ])
    `;

    const goban = new Goban({
      'size': 19,
      'width': 800,
      'sgf': sgf
    });
    
  </script>
```
<a href="https://maksimkorzh.github.io/gobanjs/load_sgf.html">see example...</a>
