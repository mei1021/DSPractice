
     //設定基本資料 

    let firstName = Html('input')
    .setClass('input')
    .setAttribute('placeholder','莫小豬')
    .setAttribute('id','name')
    .setAttribute('type','text');

    let firstp = Html('p')
    .setClass('control')
    .appendChild(firstName.node);


    //設定名字 
  
    let firstLabel = Html('label')
    .setClass('control-label')
    .setAttribute('HTML_For','name')
    .setAttribute('innerHTML','姓名');
  
    let firstdiv = Html('div')
    .setClass('h-field')
    .appendChild(firstLabel.node)
    .appendChild(firstp.node);
    


    //生命值 
    let secondName = Html('input')
    .setClass('input')
    .setAttribute('placeholder','15')
    .setAttribute('id','hp')
    .setAttribute('type','number');

    let secondp = Html('p')
    .setClass('control')
    .appendChild(secondName.node);

    let secondLabel = Html('label')
    .setClass('control-label')
    .setAttribute('HTML_For','hp')
    .setAttribute('innerHTML','血量(hp)');

    let seconddiv = Html('div')
    .setClass('h-field')
    .appendChild(secondLabel.node)
    .appendChild(secondp.node);


    // ap
    
    let thirdName = Html('input')
    .setClass(thirdName_input)
    .setAttribute('placeholder','2')
    .setAttribute('id','ap')
    .setAttribute('type','NB');

    let thirdp = Html('p')
    .setClass(control)
    .appendChild(thirdName.node);

    let thirdLabel = Html('label')
    .setClass('third_label')
    .setAttribute('HTML_For','ap')
    .setAttribute('innerHTML','攻擊力(ap)')

    let thirddiv = Html('div')
    .setClass('h-field')
    .appendChild(thirdp.node)
    .appendChild(thirdLabel.node);



     // dp

    let fourName = Html('input')
    .setClass('input')
    .setAttribute('placeholder','1')
    .setAttribute('id','dp')
    .setAttribute('type','NB');

    let fourp = Html('p')
    .setClass('control')
    .appendChild(fourName.node);

    let fourLabel = Html('label')
    .setClass('four_label')
    .setAttribute('HTML_For','dp')
    .setAttribute('innerHTML','防禦力(dp)');

    let fourdiv = Html('div')
    .setClass('h-field')
    .appendChild(fourp.node)
    .appendChild(fourLabel);

    //主程式

    let main = Html('div')
    .setClass('main')
    .appendChild(firstdiv.node)
    .appendChild(seconddiv.node)
    .appendChild(thirddiv.node)
    .appendChild(fourdiv.node);


   

  // 準備承載 *網頁內容* 的 HTML 元素
  let cardContent = Html('article')
    .setClass('card-content')
    .appendChild(main.node); //從這呼叫main

  // 準備 *網頁桌面* 的 HTML 元素
  let cardDesktop = Html('section')
    .setClass('card')
    .appendChild(cardHeader.node)   // 將 *網頁版頭* 放上 *網頁桌面*
    .appendChild(cardContent.node); // 把呼叫main的內容out到網頁

  // 將 *網頁桌面* 放上 *網頁*
  let desktop = document
    .querySelector('.site-body')
    .appendChild(cardDesktop.node);

  /*
   滑鼠游標移動追蹤 
   */
  desktop.addEventListener('mousemove', (e) => {
    document.getElementById('cursor-x').textContent = e.clientX;
    document.getElementById('cursor-y').textContent = e.clientY;
  });
});
