<html>
  <style>

.mycards {
  z-index: 3;
  text-align: left;
  display: flex;
  flex-flow: row wrap;
  justify-content: space-evenly;
  margin-top: 10px;
}
.mycard {
  word-wrap: break-word;
  background-color: #fff;
  margin: 10px;
  width: var(--image-size);
  height: calc(var(--image-size) + 33px);
  text-align: left;
  background: #ffffff;
  background-clip: border-box;
  position:relative;
}
.mycard img {
  height: var(--image-size) !important;
  width: var(--image-size) !important;
  cursor: pointer;
  border-radius: 4px;
  box-shadow: 2px 2px 6px 0px  rgba(0,0,0,0.3);
}  
.mycard .icon-row {
  position: absolute;
  background: white;
  cursor: pointer;
  bottom: 33px;
  right: 0px;
  opacity:0.7;
  border-radius: 3px;
}
.mycard.card-title {
  position: relative;
  background: #fff;
  margin-top: 0px;
  margin-bottom:5px;
  height:35px;
  padding-left:5px;
  padding-right:5px;
  cursor: pointer;
}
.mycard h2 {
  font-weight: 800;
  height:15px;
  overflow:hidden;
  text-overflow: ellipsis;
  text-align: left;
  vertical-align: top;
  font: 12px Helvetica, Verdana, sans-serif;
}
  </style>
 </html>

<html>
  <div class="mycard" id="1678475623504">
    <a href="/album#1678475623504" target="_blank">
      <img data-src="https://storage.googleapis.com/cloudplayer/artwork/1678475623504" loading="lazy" src="https://storage.googleapis.com/cloudplayer/artwork/1678475623504">
    </a>
    <div class="card-title">
    <h2><b>J.J. Johnson / Clifford Brown</b></h2>
    <h2>[2014] Jay Jay Johnson With Clifford Brown</h2>
    </div>
  </div>
</html>
