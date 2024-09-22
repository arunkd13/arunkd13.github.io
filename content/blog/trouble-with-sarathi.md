+++
title = "Trouble with Sarathi"
taxonomies.tags = ["life"]
date = 2024-09-22
+++

I had to renew my wife's driving license which was issued at Tindivanam RTO.
Unfortunately, it was not uploaded into the computerised records at that time.
On enquiring in a local Driving School, they asked to visit the concerned RTO
and request them to upload the details into the system. How many countless hours
of human life wasted, with each person having to request individually!

I visited the RTO in person and the letter receiving clerk asked to write a
letter as he is wont. Accepting the letter and a copy of the license, he said,
that I would receive an SMS in a
week or so after it is uploaded.

I never got any SMS even after 2 weeks. On
checking the driving license in the Parivahan portal, it showed an application
number and it was pending approval.

Another visit to the RTO, this time, by my father-in-law and the answer was that
there was some delay and they would upload in a few days.

Once again, I never received any SMS after that, and without a proper way of
knowing the status, I was resigned to have someone visit the RTO once again.

I decided to check the status on the website before any further visit, and saw a
link to view the application status, mentioned on the [Parivahan Sarathi
portal](https://sarathi.parivahan.gov.in/sarathiservice/stateSelection.do). I
was excited and decided to view the status, but the site was frustratingly slow.
I even disabled [uBlock Origin](https://en.wikipedia.org/wiki/UBlock_Origin),
suspecting that some _critical_ bloatware was causing problems. But still the
website was slow. Looked like the application was blocked on me for uploading
the required documents. When I tried to upload them
it errored out and the site hanging on every step was making it difficult to
figure out why it was erroring.

Out of frustration, I decided to dig a bit deeper into why the site was slow and
opened the Web Developer Tools on Firefox. I was able to see calls to
_vani-hyd.nic.in_ hanging and timing out after a few minutes. This was the
reason for the website being slow. I also realized, this might not be critical
part, as after time out I was able to proceed to further steps. On right
clicking the URL in the request list, I noticed that there was an option to
block it.

I got excited that finally there could be a way to upload the documents and
complete my part of the application process. On uploading the document again, it
still errored, but on reading the page more attentively, it was mentioned that the file size
should be less than 500 KB. A quick processing step with Ghostscript brought the file
size down within limits.

    gs -sDEVICE=pdfwrite -dCompatibilityLevel=1.4 -dPDFSETTINGS=/ebook -dNOPAUSE -dQUIET -dBATCH -sOutputFile=output.pdf input.pdf

Now it was all smoothing sailing and the upload process succeeded, though it
abruptly landed ont he initial status request page without any mention of the
happy news. I had to once again key the application number and the captcha and
there it listed that the further actions were on the RTO.

I don't think everyone would be able to complete this step without
seeking assistance from a third party like a driving school. Looks like Digital
India instead of improving things, has just added another layer of
private intermediaries between the government and the citizen.
