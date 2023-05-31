<script>
export default {
    emits: ['response'],
    created() {
        this.$emit('response', 'hello from child')
    }
}
</script>

<template>
    <div class="wholeContainer">
        <div class="uiContainer">
            <div class="leftContainer">
                <div class="header">
                    <div class="titlediv">
                        <h1 class="title">Welcome back!</h1>
                    </div>
                    <div class="titlediv">
                        <p class="subtitle">We're so excited to see you again!</p>
                    </div>
                </div>

                <div class="inputContainer">
                    <div class="discdiv">
                        <h1 class="disc">
                            EMAIL OR PHONE NUMBER
                            <h1 class="disc" style="color: red">*</h1>
                        </h1>
                    </div>
                    <label for="email"></label>
                    <input class="input" type="email" id="email" spellcheck="false">

                    <br>

                    <div class="discdiv">
                        <h1 class="disc">
                            PASSWORD
                            <h1 class="disc" style="color: red">*</h1>
                        </h1>
                    </div>
                    <label for="password"></label>
                    <input class="input" type="password" id="password" spellcheck="false">

                    <div>
                        <a href="https://youtube.com" class="hyperlink">Forgot your password?</a>
                    </div>

                    <br>

                    <button class="logIn" id="logInButton"><b>Log In</b></button>

                    <p class="bruh">
                        Need an account?
                        <a href="https://youtube.com" class="hyperlink"> Register</a>
                    </p>
                </div>
            </div>

            <div class="rightContainer">
                <div class="imagediv">
                    <img src="/src/qr-code.png" class="qrCode">
                </div>

                <br><br>

                <div class="header">
                    <div class="titlediv">
                        <h1 class="title">Log in with QR Code</h1>
                    </div>
                    <div class="titlediv">
                        <p class="subtitle">
                            Scan this with the <b>Discord mobile<br>
                                app</b> to log in instantly.
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.backgroundImage {
    position: absolute;
    width: 100vw;
    min-height: 100vh;
    overflow: auto;
    top: 0;
    left: 0;
}

.wholeContainer {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    min-height: 100vh;
    height: 100%;
    display: flex;
    justify-content: center;
    align-content: center;
}

.uiContainer {
    top:50%;
    transform: translate(0%,-50%);
    position: absolute;
    width: 780px;
    height: 450px;
    background-color: #313338;
    border-radius: 5px;
    display: flex;
    flex-direction: row;
}

.leftContainer {
    width: 60%;
    height: 100%;
    display: flex;
    flex-direction: column;
    padding-top: 30px;
    padding-left: 40px;
    padding-right: 40px;
}

.header {
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-content: center;
}

.titlediv {
    width: 100%;
    display: flex;
    justify-content: center;
    align-content: center;
    height: fit-content;
}

.title {
    position: relative;
    font-family: "ABC Ginto Nord","Noto Sans","Helvetica Neue",Helvetica,Arial,sans-serif;
    color: #F2F3F5;
    font-size: 23px;
    margin-block-start: 0;
    margin-block-end: 12px;
}

.subtitle {
    position: relative;
    font-family: "ABC Ginto Nord","Noto Sans","Helvetica Neue",Helvetica,Arial,sans-serif;
    color: #B5BAC1;
    margin-block-start: 0;
    text-align: center;
}

.inputContainer {
    display: flex;
    flex-direction: column;
}

.disc {
    font-family: "ABC Ginto Nord","Noto Sans","Helvetica Neue",Helvetica,Arial,sans-serif;
    color: #B5BAC1;
    font-size: 12px;
    display: flex;
    flex-direction: row;
    padding-right: 3px;
}

.discdiv {
    display: flex;
    flex-direction: row;
}

.input {
    background-color: #1E1F22;
    border: none;
    outline: 0;
    height: 40px;
    color: #F2F3F5;
    border-radius: 3px;
}

.hyperlink {
    color: #01A6F8;
    font-family: "ABC Ginto Nord","Noto Sans","Helvetica Neue",Helvetica,Arial,sans-serif;
    font-size: 14px;
    text-decoration: none;
}

.hyperlink:visited {
    text-decoration: none;
}

.logIn {
    border-radius: 2px;
    border: 0;
    background-color: #5865F2;
    height: 50px;
    color: #F2F3F5;
    font-size: 15px;
    transition-duration: 0.3s;
}

.bruh {
    font-family: "ABC Ginto Nord","Noto Sans","Helvetica Neue",Helvetica,Arial,sans-serif;
    color: #939AA3;
    font-size: 14px;
}

.logIn:hover {
    background-color: #4752C4;
}

.rightContainer {
    width: 40%;
    height: 100%;
    flex-direction: column;
    padding-top: 60px;
    padding-right: 20px;
}

.imagediv {
    width: 100%;
    display: flex;
    justify-content: center;
    align-content: center;
}

.qrCode {
    height: 180px;
    width: 180px;
    border-radius: 5px;
}

</style>