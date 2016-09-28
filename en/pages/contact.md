---
category: Miscellaneous
description: A contact form to reach us.
icon: user_telephone
keywords: Memba, Kidoju, software, education, teach, learn, study, knowledge, test, quiz, contact
language: en
title: Contact Us
uuid: 0c62866f-a8e7-491c-9236-cf61b0a986ee
author: jlchereau
author_url: https://github.com/jlchereau
avatar_url: https://avatars.githubusercontent.com/u/2556751?v=3
edit_url: https://github.com/kidoju/support.kidoju.com/blob/master/en/pages/contact.md
site_url: https://www.kidoju.com/support/en/contact
creation_date: 2016-04-12T08:56:29Z
---
<div class="container">
    <div class="row">
        <div class="col-sm-8">
            <form name="insightly_web_to_contact" action="https://iuqqkh1d.insight.ly/WebToContact/Create" method="post">
                <input type="hidden" name="formId" value="LfOfVxwkqgkYOx7pcM6LtA=="/>
                <div class="form-group">
                    <label for="insightly_firstName">First Name: </label>
                    <input id="insightly_firstName" name="FirstName" type="text" class="k-textbox" style="width: 100%"
                     pattern="^[^<>\/]{3,50}$" validationMessage="Please enter your first name of 3 to 50 characters without forbidden symbol.">
                </div>
                <div class="form-group">
                    <label for="insightly_lastName">Last Name: </label>
                    <input id="insightly_lastName" name="LastName" type="text" class="k-textbox" style="width: 100%"
                     pattern="^[^<>\/]{3,50}$" validationMessage="Please enter your last name of 3 to 50 characters without forbidden symbol.">
                </div>
                <div class="form-group">
                    <label for="insightly_organization">Organisation: </label>
                    <input id="insightly_organization" name="Organization" type="text" class="k-textbox" style="width: 100%"
                     pattern="^([^<>\/]{3,50})?$" validationMessage="Please enter your organisation of 3 to 50 characters without forbidden symbol.">
                </div>
                <div class="form-group">
                    <label for="insightly_role">Role: </label>
                    <input id="insightly_role" name="Role" type="text" class="k-textbox" style="width: 100%"
                     pattern="^([^<>\/]{3,50})?$" validationMessage="Please enter your role of 3 to 50 characters without forbidden symbol.">
                </div>
                <div class="form-group">
                    <input type="hidden" name="emails[0].Label" value="Work">
                    <label for="email[0]_Value">E-mail: </label>
                    <input id="emails[0]_Value" name="emails[0].Value" type="email" class="k-textbox" style="width: 100%"
                    required validationMessage="Please enter your email.">
                </div>
                <div class="form-group">
                    <input type="hidden" name="phones[0].Label" value="Work">
                    <label for="phones[0]_Value">Phone: </label>
                    <input id="phones[0]_Value" name="phones[0].Value" type="text" class="k-textbox" style="width: 100%"                    
                    pattern="^([0-9 \-\+]{6,20})?$" validationMessage="Please enter your phone number of 6 to 20 characters.">
                </div>
                <div class="form-group">
                    <label for="insightly_background">Message: </label>
                    <textarea id="insightly_background" name="background" class="k-textbox" style="width: 100%; height: 150px; resize: vertical"
                    pattern="^[^<>\/]{10,500}$" validationMessage="Please enter your message of 10 to 500 characters without forbidden symbol."></textarea>
                </div>
                <div class="form-group">
                    <input type="submit" value="Submit" class="k-button k-primary pull-right">
                </div>
            </form>
        </div>
        <div class="col-sm-4">
            <p><strong>Or write us at:</strong></p>
            <address>
                Memba Sarl<br/>
                20 avenue Pasteur<br/>
                L-2310 Luxembourg
            </address>
        </div>
    </div>
</div>


<script>
;(function (window, $, undefined) {

    if ($.fn.kendoValidator) {
        var form = $('#insightly_web_to_contact');
        var validator = form.kendoValidator().data('kendoValidator');
        form.submit(function (e) {
            if (!validator.validate()) {
                e.preventDefault();
            }
        });
    }

}(this, jQuery));
</script>