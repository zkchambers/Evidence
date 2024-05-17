# Email Validation

<!-- Image -->

Code:       <input
                      type="email"
                      class="form-control"
                      placeholder="example@company.com"
                      pattern="^([a-zA-Z0-9_\-\.]+)@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.)|(([a-zA-Z0-9\-]+\.)+))([a-zA-Z]{2,4}|[0-9]{1,3})(\]?)$"
                      size="30"
                      id="email"
                      name="email"
                      required
                    />

I created the pattern for the input in the email form, which ensure that there is a .com, .org, .edu etc in the email and if it doesn't it will ask the user fill the form out with the correct information