+++
title = "Trouble with Sarathi"
taxonomies.tags = ["life"]
date = 2024-09-22
+++

I had to renew my wife's driving licence which was issued at Tindivanam RTO.
Unfortunately, it was not uploaded into the computerized records at the time it
was issued, and it was a prerequisite for renewing the licence from a different
RTO other than the one where it was issued.

On enquiring at a local driving school, they asked to visit the concerned RTO
and request them to upload the details into the system. Half done digitization,
and countless hours of human life wasted, with each person having to make a request
individually!

I visited the RTO in person and the letter receiving clerk asked to write a
letter as he is wont. Accepting the letter and a copy of the licence, he
dismissed me saying that I will receive an SMS in a week or so after it is
uploaded.

I never got any SMS even after 2 weeks. On checking the driving licence in the
[Parivahan Sarathi portal](https://sarathi.parivahan.gov.in/sarathiservice/stateSelection.do), it
showed an application number, and it was pending approval.

Another visit to the RTO, this time, by my father-in-law and the answer was that
there was some delay in the server, and they would upload it in a few days.

Once again, I never received any SMS after that, and without a proper way of
knowing the status, I was resigned to have someone visit the RTO once again.

I decided to check the status one last time, before the imminent visit, but the
site was frustratingly slow. I even disabled [uBlock
Origin](https://en.wikipedia.org/wiki/UBlock_Origin),
suspecting that some _critical_ bloatware was causing problems. But still the
website was slow. Finally, when I got to the view the status, it showed that the
application was blocked on me for uploading the required documents. When I tried
to upload them, it errored out and the site hanging on every step was
making it even more difficult to figure out why I got the error.

Out of frustration, I decided to dig a bit deeper into the site, and
opened the Web Developer Tools on Firefox. I was able to see calls to
_vani-hyd.nic.in_ hanging and timing out after a few minutes—this was the
reason the website was slow. I also realized, this might not be a critical
part as, after time out I was able to proceed to further steps. On
right-clicking the URL in the request list, I noticed that there was an option
to block it.

This was exactly what I needed! I was excited by the possibility of me
finally completing my part of the application process—uploading the documents.
On finishing that step, it still errored. Cursing the software developers who built the
website, I began reading the page more attentively. Hidden in the verbiage of
instructions, it was mentioned that the file size should be less than 500 KB.

A quick processing step with Ghostscript brought the file size down, within
limits.

    gs -sDEVICE=pdfwrite -dCompatibilityLevel=1.4 -dPDFSETTINGS=/ebook -dNOPAUSE -dQUIET -dBATCH -sOutputFile=output.pdf input.pdf

Now it was all smoothing sailing and the upload process succeeded, though it
abruptly landed on the initial status request page without any mention of the
happy news. I had to once again key the application number and the captcha to
find the updated status—further actions were on the RTO.

I don't think everyone would be able to complete this step without
seeking assistance from a third party like a driving school. Looks like Digital
India instead of improving things, has just added another layer of
private intermediaries between the government and the citizen.

The process took another 3 weeks, where my computer skills didn't help, and my
father-in-law had to still visit the RTO to prod the officers into action. The
clerk was kind enough to give his phone number, so that, we could remind him
over the phone, instead of a direct visit.

The only nice part of the whole process was that, there was no direct ask for a
bribe to speed things up. The clerk and the officer were trying to genuinely
complete the process, though hampered by inefficient systems and their lack
of skill.