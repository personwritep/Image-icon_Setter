// ==UserScript==
// @name        Image-icon Setter ⭐
// @namespace        http://tampermonkey.net/
// @version        0.1
// @description        ブログ編集画面でアイコン画像のレイアウトを最適化する
// @author        Ameba Blog User
// @match        https://blog.ameba.jp/ucs/entry/srventryinsertinput.do*
// @match        https://blog.ameba.jp/ucs/entry/srventryupdateinput.do*
// @icon        https://www.google.com/s2/favicons?sz=64&domain=ameba.jp
// @grant        none
// @updateURL        https://github.com/personwritep/Image-icon_Setter/raw/main/Image-icon_Setter.user.js
// @downloadURL        https://github.com/personwritep/Image-icon_Setter/raw/main/Image-icon_Setter.user.js
// ==/UserScript==


let retry=0;
let interval=setInterval(wait_target, 20);
function wait_target(){
    retry++;
    if(retry>100){ // リトライ制限 100回 2sec
        clearInterval(interval); }
    let target=document.getElementById('cke_1_contents'); // 監視 target
    if(target){
        clearInterval(interval);
        main(target); }}


function main(target){

    let monitor=new MutationObserver(set_img);
    monitor.observe(target, {childList: true});

    set_img();

    function set_img(){
        let editor_iframe=document.querySelector('.cke_wysiwyg_frame');
        if(editor_iframe){ // iframe読込みが実行条件
            let iframe_doc=editor_iframe.contentWindow.document;
            if(iframe_doc){
                iframe_doc.addEventListener('click', function(event){
                    if(event.shiftKey){ // アイコン画像を「Shift+左Click」
                        let elem=iframe_doc.elementFromPoint(event.clientX, event.clientY);
                        let img_elem=elem.closest('img');
                        if(img_elem){ // 24×24pxの画像でアメーバ絵文字を省く
                            if(img_elem.width=='24' && !img_elem.src.includes('/img/char/')){
                                event.preventDefault();
                                event.stopImmediatePropagation();

                                img_elem.setAttribute('alt', 'icon');
                                img_elem.style.cssText="margin-top: -2px; vertical-align: -6px;";

                                let p_elem=img_elem.closest('p');
                                if(p_elem){
                                    p_elem.style.removeProperty('text-align'); }

                                let link_elem=img_elem.closest('a');
                                if(link_elem){
                                    link_elem.replaceWith(...link_elem.childNodes); }

                            } // if()

                        }}}, { capture: true });

            }}} // set_img()

} // main()
