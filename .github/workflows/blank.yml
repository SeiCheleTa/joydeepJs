//declearing global variable
var nodeList;
var select = function (selector) {
    return new libraryName(selector);
};


function libraryName(selector) {
    if (selector == document) {
        nodeList == document;
    }
    else {
        nodeList = document.querySelectorAll(selector);
    }
    return this;
}
libraryName.prototype.find = function (name) {

    return nodeList = nodeList[0].querySelector(name);

}
libraryName.prototype.inside = function (html) {

    nodeList.forEach(node => { node.innerHTML = html; })


}

libraryName.prototype.style = function (property) {
    nodeList.forEach(node => {
        if (node.hasAttribute("style")) {
            var propertyone = node.getAttribute("style");
            var newproperty = propertyone + property;
            node.setAttribute("style", newproperty);
        }
        else {
            node.setAttribute("style", property);
        }

    })
}

libraryName.prototype.hide = function () {
    nodeList.forEach(node => { node.style.display = 'none'; })
}

libraryName.prototype.show = function () {
    nodeList.forEach(node => { node.style.display = 'block'; })
}
libraryName.prototype.on = function (action, function_) {
    nodeList.forEach(node => { node.addEventListener(action, function_); })

}
libraryName.prototype.click = function (function_) {
    nodeList.forEach(node => { node.addEventListener("click", function_); })

}
libraryName.prototype.keyup = function (function_) {
    nodeList.forEach(node => { node.addEventListener("keyup", function_); })

}
libraryName.prototype.ready = function (function_) {
    document.addEventListener("DOMContentLoaded", function_);

}
libraryName.prototype.addClass = function (className) {
    nodeList.forEach(node => { node.classList.add(className); })

}
libraryName.prototype.removeClass = function (className) {
    nodeList.forEach(node => { node.classList.remove(className); })

}
libraryName.prototype.attr = function (name, value) {
    if (value) {
        nodeList.forEach(node => { node.setAttribute(name, value); })
    } else {

        return nodeList[0].getAttribute(name);
    }

}

//ajax function
function ajax(myJSON) {
    const myObj = myJSON;
    url = myObj["url"];
    method = myObj["method"];
    success = myObj["success"];
    fail = myObj["fail"];
    percent = myObj['progressPercent'];
    const xhttp = new XMLHttpRequest();
    xhttp.onload = function () {
        var response;
        if (this.readyState == 4 && this.status == 200) {
            response = this.responseText;
            return success(response);
        } else {
            if (this.status == 403) {
                error = url + " 403 (Forbidden)";
                if (myObj["errors"]) {
                    console.log(error);
                }
            }
            if (this.status == 404) {
                error = url + " 400 (Page not found)";
                if (myObj["errors"]) {
                    console.log(error);
                }
            }
            return fail(error);
        }
    }
    xhttp.upload.onprogress = function (evt) {

        let percentComplete = evt.loaded / evt.total * 100 + '%';
        return percent(percentComplete);
    }
    parameters = '';
    var obj = myObj["data"];
    var count = Object.keys(obj).length;
    for (i = 0; i < count; i++) {
        parameters += Object.keys(obj)[i] + '=' + obj[Object.keys(obj)[i]] + '&';
    }
    if (method == 'POST' || method == 'post' || method == 'Post') {
        xhttp.open("POST", url, true);
        xhttp.setRequestHeader("Content-type", "application/x-www-form-urlencoded");
        xhttp.send(parameters);
    } else {
        xhttp.open("GET", url, true);
        xhttp.setRequestHeader("X-Requested-With", "XMLHttpRequest");
        xhttp.send();
    }
}
//shortcut functions
//len
function len(str) {
    let len = str.lenght;
    return len;
}
//find max
function max() {
    let max = -Infinity;
    for (let i = 0; i < arguments.length; i++) {
        if (arguments[i] > max) {
            max = arguments[i];
        }
    }
    return max;
}
//sum
function sum() {
    let sum = 0;
    for (let i = 0; i < arguments.length; i++) {
        sum += arguments[i];
    }
    return sum;
}
