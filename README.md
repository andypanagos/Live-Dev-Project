# Live-Dev-Project


# C# Live Project

### Introduction

I recently participated in my second live project with The Tech Academy for the Software
Developer Bootcamp. I was given the opportunity to do a two week sprint with a team
consisting of instructors and peers. The project was built using the ASP .NET MVC and Entity Framework.
This was the second time in my young development career working in a professional environment with peers,
something I am certainly beginning to enjoy. I personally had the chance to work on front end stories as well as
back end utilizing C# razor syntax, HTML, CSS, Javascript, JQUERY, AJAX and BOOTSTRAP. Below you can view snippets the stories I completed during the project.







## Front End Stories

#### Style The Home Page

For this story I was asked to create and style a home page for 
movie theatre's webpage. The client asked for the displayal of the spotlight, donations, and sponsors
areas. With a functional "Donate Now" button.  


## HTML

```

@{
  ViewBag.Title = "Home Page";
}

<div>
    <p class="Home-Index-Logo"><img src="~/Content/images/TheatreLogo.png" /></p>
    @*<p class="lead">ASP.NET is a free web framework for building great Web sites and Web applications using HTML, CSS and JavaScript.</p>*@
    @*<p><a href="https://asp.net" class="btn btn-primary btn-lg">Learn more &raquo;</a></p>*@
</div>


<body>
    <div class="container">
        <div class="Home-Index-AllContent">
            <div class="row">
                <div class="col-8">
                    <h4 class="Home-Index-UnderlineText">SPOTLIGHT</h4>
                    <br />
                    <p><img src="~/Content/images/MidsummerNightDream.png"</p>
                    <p><img src="~/Content/images/Tempest.png"</p>
                    </br>
                    <h4 class="Home-Index-UnderlineText">LAND ACKNOWLEDGEMENT</h4>
                    <br />
                    <p>
                        Founded by the community, for the community, NAYA is a family of numerous tribes and voices who are rooted in sustaining tradition and building cultural wealth.
                        We provide culturally-specific programs and services that guide our people in the direction of personal success and balance through cultural empowerment.
                        Our continuum of lifetime services create a wraparound,
                        holistic healthy environment that is Youth Centered, Family Driven, Elder Guided.
                    </p>
                </div>
                <div class="col-4">
                    <h4 class="Home-Index-UnderlineText">DONATIONS</h4>
                    <br />
                    <button onclick="" class="btn btn-lg Home-Index-Button">Click To Support!</button>
                    <div class="Home-Index-Sponsor">
                        <h4 class="Home-Index-UnderlineText">SPONSORS</h4>
                        <br />
                        <p>
                            <img class="Home-Index-SponsorImageWide" src="~/Content/images/Sponsors/Ellyn-Bye-Logo.png" />
                            <img class="Home-Index-SponsorImage" src="~/Content/images/Sponsors/LogoRoundColor.png" />
                            <img class="Home-Index-SponsorImage" src="~/Content/images/Sponsors/Ninkasi-white-text.png" />
                            <img class="Home-Index-SponsorImageWide" src="~/Content/images/Sponsors/OCF-logo-in-white-with-tagline-lg.png" />
                            <img class="Home-Index-SponsorImageWide" src="~/Content/images/Sponsors/RACC.png" />
                        </p>
                    </div>
                    <div class="Home-Index-LandAcknowledgement">
                        <a href="https://nayapdx.org/" target="_blank">
                            <p><img class="Home-Index-NAYA" src="~/Content/images/NAYAFamilyCenter.jpg"</p>
                        </a>
                        <p>
                            Click to visit the NAYA Family Center to learn more about
                            supporting our local indigenous communities.
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</body>

```

## CSS

```

.Home-Index-Logo {
    text-align: center;
    padding-top: 50px;
    padding-bottom: 20px;
}

.Home-Index-AllContent {
    padding-top: 50px;
}

.Home-Index-Button {
    background-color: var(--main-color);
    color: white;
}


.Home-Index-SponsorImage {
    height: 67px;
    width: 67px;
}

.Home-Index-SponsorImageWide {
    height: 67px;
    width: fit-content;
}

.Home-Index-UnderlineText {
    text-decoration: underline;
}

.Home-Index-Sponsor {
    padding-top: 40px;
}

.Home-Index-NAYA {
    height: 256px;
    width: 256px;
}

.Home-Index-LandAcknowledgement {
    padding-top: 500px;
}

```
## Style CRUD pages

### CSS

```
.CastMember-CreateEdit-FormStyle {
    width: 50%;
    margin: 0 auto;
    padding-top: 10px;
    background-color: var(--main-color--light);
    border-radius: 10px;
    box-shadow: 1px 1px 3px var(--main-color), -1px -1px 0px var(--light-color);
    text-align: center
}

.CastMember-CreateEdit-Labels {
    padding: 10px;
    max-width: 80%;
    margin: 0 auto;
    text-align: center;
}

.CastMember-CreateEdit-Div {
    padding: 10px;
    max-width: 80%;
    margin: 0 auto;
    text-align: center;
}

CastMember-CreateEdit-Photo {
    padding: 10px;
    max-width: 50%;
    margin: 0 auto;
    text-align: center;
}

.CastMember-CreateEdit-Placeholder {
    background-color: white;
    border: 1px solid black;
}

.CastMember-CreateEdit-Header {
    color: var(--secondary-color);
    text-align: center;
    margin-bottom: 25px;
    padding-top: 50px;
}

.CastMember-CreateEdit-BackButton {
    background-color: var(--light-color);
    font-weight: bold;
    margin-bottom: 7px;
    border-radius: 7px;
    box-shadow: 1px 1px 3px var(--main-color), -1px -1px 0px var(--light-color);
}

.CastMember-CreateEdit-CreateButton {
    background-color: var(--secondary-color);
    font-weight: bold;
    margin-bottom: 7px;
}

```


## Back End Stories

For the back end stories, my job was to create functional CRUD pages
which would create, edit and delete cast members in movies.

## Model and CRUD Pages

```

public class CastMember
    {
        public int CastMemberId { get; set; }
        public string Name { get; set; }
        public int YearJoined { get; set; }
        public string MainRole { get; set; }
        public string Bio { get; set; }
        //public Byte[] Photo { get; set; }
        public bool CurrentMember { get; set; }
        public string Character { get; set; }
        public int CastYearLeft { get; set; }
        public int DebutYear { get; set; }
    }


public class CastMemberController : Controller
    {
        private ApplicationDbContext db = new ApplicationDbContext();
        // GET: Prod/CastMember
        public ActionResult Index()
        {
            return View(db.CastMembers.ToList());
        }


        public ActionResult Create()
        {
            return View();
        }

        [HttpPost]
        [ValidateAntiForgeryToken]
        public ActionResult Create(string firstName, int yearJoined, string mainRole, string myBio, bool currentMember, string myCharacter, int castYearLeft, int debutYear)
        {
            using (ApplicationDbContext db = new ApplicationDbContext())
            {
                var castmember = new CastMember();
                castmember.Name = firstName;
                castmember.YearJoined = Convert.ToInt32(yearJoined);
                castmember.MainRole = mainRole;
                castmember.Bio = myBio;
                castmember.CurrentMember = Convert.ToBoolean(currentMember);
                castmember.Character = myCharacter;
                castmember.CastYearLeft = castYearLeft;
                castmember.DebutYear = debutYear;

                db.CastMembers.Add(castmember);
                db.SaveChanges();
            }
            return View();
        }


        public ActionResult Edit(int? id)
        {
            if (id == null)
            {
                return new HttpStatusCodeResult(HttpStatusCode.BadRequest);
            }
            CastMember member = db.CastMembers.Find(id);
            if (member == null)
            {
                return HttpNotFound();
            }
            return View(member);
        }

        [HttpPost]
        [ValidateAntiForgeryToken]
        public ActionResult Edit(string firstName, int yearJoined, string mainRole, string myBio, bool currentMember, string myCharacter, int castYearLeft, int debutYear)
        {
            using (ApplicationDbContext db = new ApplicationDbContext())
            {
                var castmember = new CastMember();
                castmember.Name = firstName;
                castmember.YearJoined = Convert.ToInt32(yearJoined);
                castmember.MainRole = mainRole;
                castmember.Bio = myBio;
                castmember.CurrentMember = Convert.ToBoolean(currentMember);
                castmember.Character = myCharacter;
                castmember.CastYearLeft = castYearLeft;
                castmember.DebutYear = debutYear;

                db.Entry(castmember).State = EntityState.Modified;
                db.SaveChanges();
                return RedirectToAction("Index");
            }
        }



        public ActionResult Delete(int? id)
        {
            if (id == null)
            {
                return new HttpStatusCodeResult(HttpStatusCode.BadRequest);
            }
            CastMember member = db.CastMembers.Find(id);
            if (member == null)
            {
                return HttpNotFound();
            }
            return View(member);
        }

        [HttpPost, ActionName("Delete")]
        [ValidateAntiForgeryToken]
        public ActionResult DeleteConfirmed(int id)
        {
            CastMember member = db.CastMembers.Find(id);
            db.CastMembers.Remove(member);
            db.SaveChanges();
            return RedirectToAction("Index");
        }

        protected override void Dispose(bool disposing)
        {
            if (disposing)
            {
                db.Dispose();
            }
            base.Dispose(disposing);
        }
    }

```



## Other Skills I've Learned

* How to work in a professional environment with peers, my ability to work within a team
and complete the tasks at hand when asked, as well as how to overcome any obstacles and utilize 
resources provided in my environment to move forward.

* Practicing good version control within Visual Studio

* Time management. Being able to complete the two week sprint while working a full time job was a complete hustle,
never let it be a struggle. 
