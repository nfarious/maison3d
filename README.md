# Interactive 3D House - Rotations and Displacements
This project draws a 3D house and provices user adjustable sliders to displace or rotate it along the x, y, and z axes.

Each of the house vertices must undergo three rotations along the axes using the following rotation matrix:

<math xmlns="http://www.w3.org/1998/Math/MathML">
  <mstyle displaystyle="true">
    <mrow class="MJX-TeXAtom-ORD">
      <msub>
        <mi>x</mi>
        <mrow class="MJX-TeXAtom-ORD">
          <mi>r</mi>
          <mi>o</mi>
          <mi>t</mi>
        </mrow>
      </msub>
      <mo>=</mo>
      <mi>&#x03D5;<!-- ϕ --></mi>
      <mo>,</mo>
      <mspace width="1em" />
      <msub>
        <mi>y</mi>
        <mrow class="MJX-TeXAtom-ORD">
          <mi>r</mi>
          <mi>o</mi>
          <mi>t</mi>
        </mrow>
      </msub>
      <mo>=</mo>
      <mi>&#x03C8;<!-- ψ --></mi>
      <mo>,</mo>
      <mspace width="1em" />
      <msub>
        <mi>z</mi>
        <mrow class="MJX-TeXAtom-ORD">
          <mi>r</mi>
          <mi>o</mi>
          <mi>t</mi>
        </mrow>
      </msub>
      <mo>=</mo>
      <mi>&#x03B8;<!-- θ --></mi>
      <mo linebreak="newline"></mo>
    </mrow>
  </mstyle>
</math>

<math>
  <mstyle displaystyle="true">
    <mrow>
      <msub>
        <mi>c</mi>
        <mrow class="MJX-TeXAtom-ORD">
          <mi>x</mi>
        </mrow>
      </msub>
      <mo>=</mo>
      <mi>c</mi>
      <mi>o</mi>
      <mi>s</mi>
      <mo stretchy="false">(</mo>
      <mi>&#x03D5;<!-- ϕ --></mi>
      <mo stretchy="false">)</mo>
      <mo>,</mo>
      <mspace width="1em" />
      <msub>
        <mi>s</mi>
        <mrow class="MJX-TeXAtom-ORD">
          <mi>x</mi>
        </mrow>
      </msub>
      <mo>=</mo>
      <mi>s</mi>
      <mi>i</mi>
      <mi>n</mi>
      <mo stretchy="false">(</mo>
      <mi>&#x03D5;<!-- ϕ --></mi>
      <mo stretchy="false">)</mo>
      <mo linebreak="newline"></mo>
      <msub>
        <mi>c</mi>
        <mrow class="MJX-TeXAtom-ORD">
          <mi>y</mi>
        </mrow>
      </msub>
      <mo>=</mo>
      <mi>c</mi>
      <mi>o</mi>
      <mi>s</mi>
      <mo stretchy="false">(</mo>
      <mi>&#x03C8;<!-- ψ --></mi>
      <mo stretchy="false">)</mo>
      <mo>,</mo>
      <mspace width="1em" />
      <msub>
        <mi>s</mi>
        <mrow class="MJX-TeXAtom-ORD">
          <mi>y</mi>
        </mrow>
      </msub>
      <mo>=</mo>
      <mi>s</mi>
      <mi>i</mi>
      <mi>n</mi>
      <mo stretchy="false">(</mo>
      <mi>&#x03C8;<!-- ψ --></mi>
      <mo stretchy="false">)</mo>
      <mo linebreak="newline"></mo>
      <msub>
        <mi>c</mi>
        <mrow class="MJX-TeXAtom-ORD">
          <mi>z</mi>
        </mrow>
      </msub>
      <mo>=</mo>
      <mi>c</mi>
      <mi>o</mi>
      <mi>s</mi>
      <mo stretchy="false">(</mo>
      <mi>&#x03B8;<!-- θ --></mi>
      <mo stretchy="false">)</mo>
      <mo>,</mo>
      <mspace width="1em" />
      <msub>
        <mi>s</mi>
        <mrow class="MJX-TeXAtom-ORD">
          <mi>z</mi>
        </mrow>
      </msub>
      <mo>=</mo>
      <mi>s</mi>
      <mi>i</mi>
      <mi>n</mi>
      <mo stretchy="false">(</mo>
      <mi>&#x03B8;<!-- θ --></mi>
      <mo stretchy="false">)</mo>
      <mspace depth="1cm" />
      <mo linebreak="newline"></mo>
    </mrow>
  </mstyle>
</math>
<math>
  <mstyle displaystyle="true">
    <mrow>
      <msub>
        <mi>R</mi>
        <mrow class="MJX-TeXAtom-ORD">
          <mi>x</mi>
        </mrow>
      </msub>
      <mo>=</mo>
      <mrow>
        <mo>[</mo>
        <mtable rowspacing="4pt" columnspacing="1em">
          <mtr>
            <mtd>
              <mn>1</mn>
            </mtd>
            <mtd>
              <mn>0</mn>
            </mtd>
            <mtd>
              <mn>0</mn>
            </mtd>
          </mtr>
          <mtr>
            <mtd>
              <mn>0</mn>
            </mtd>
            <mtd>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>x</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <mo>&#x2212;<!-- − --></mo>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>x</mi>
                </mrow>
              </msub>
            </mtd>
          </mtr>
          <mtr>
            <mtd>
              <mn>0</mn>
            </mtd>
            <mtd>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>x</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>x</mi>
                </mrow>
              </msub>
            </mtd>
          </mtr>
        </mtable>
        <mo>]</mo>
      </mrow>
      <mspace width="1em" />
      <msub>
        <mi>R</mi>
        <mrow class="MJX-TeXAtom-ORD">
          <mi>y</mi>
        </mrow>
      </msub>
      <mo>=</mo>
      <mrow>
        <mo>[</mo>
        <mtable rowspacing="4pt" columnspacing="1em">
          <mtr>
            <mtd>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>y</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <mn>0</mn>
            </mtd>
            <mtd>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>y</mi>
                </mrow>
              </msub>
            </mtd>
          </mtr>
          <mtr>
            <mtd>
              <mn>0</mn>
            </mtd>
            <mtd>
              <mn>1</mn>
            </mtd>
            <mtd>
              <mn>0</mn>
            </mtd>
          </mtr>
          <mtr>
            <mtd>
              <mo>&#x2212;<!-- − --></mo>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>y</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <mn>0</mn>
            </mtd>
            <mtd>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>y</mi>
                </mrow>
              </msub>
            </mtd>
          </mtr>
        </mtable>
        <mo>]</mo>
      </mrow>
      <mspace width="1em" />
      <msub>
        <mi>R</mi>
        <mrow class="MJX-TeXAtom-ORD">
          <mi>z</mi>
        </mrow>
      </msub>
      <mo>=</mo>
      <mrow>
        <mo>[</mo>
        <mtable rowspacing="4pt" columnspacing="1em">
          <mtr>
            <mtd>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <mo>&#x2212;<!-- − --></mo>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <mn>0</mn>
            </mtd>
          </mtr>
          <mtr>
            <mtd>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <mn>0</mn>
            </mtd>
          </mtr>
          <mtr>
            <mtd>
              <mn>0</mn>
            </mtd>
            <mtd>
              <mn>0</mn>
            </mtd>
            <mtd>
              <mn>1</mn>
            </mtd>
          </mtr>
        </mtable>
        <mo>]</mo>
      </mrow>
      <mspace depth="1cm" />
      <mo linebreak="newline"></mo>
    </mrow>
  </mstyle>
</math>
<math>
  <mstyle displaystyle="true">
    <mrow>
      <msub>
        <mi>R</mi>
        <mrow class="MJX-TeXAtom-ORD">
          <mi>z</mi>
          <mi>y</mi>
        </mrow>
      </msub>
      <mo>=</mo>
      <msub>
        <mi>R</mi>
        <mrow class="MJX-TeXAtom-ORD">
          <mi>z</mi>
        </mrow>
      </msub>
      <mo>&#x22C5;<!-- ⋅ --></mo>
      <msub>
        <mi>R</mi>
        <mrow class="MJX-TeXAtom-ORD">
          <mi>y</mi>
        </mrow>
      </msub>
      <mo>=</mo>
      <mrow>
        <mo>[</mo>
        <mtable rowspacing="4pt" columnspacing="1em">
          <mtr>
            <mtd>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <mo>&#x2212;<!-- − --></mo>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <mn>0</mn>
            </mtd>
          </mtr>
          <mtr>
            <mtd>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <mn>0</mn>
            </mtd>
          </mtr>
          <mtr>
            <mtd>
              <mn>0</mn>
            </mtd>
            <mtd>
              <mn>0</mn>
            </mtd>
            <mtd>
              <mn>1</mn>
            </mtd>
          </mtr>
        </mtable>
        <mo>]</mo>
      </mrow>
      <mo>&#x22C5;<!-- ⋅ --></mo>
      <mrow>
        <mo>[</mo>
        <mtable rowspacing="4pt" columnspacing="1em">
          <mtr>
            <mtd>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>y</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <mn>0</mn>
            </mtd>
            <mtd>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>y</mi>
                </mrow>
              </msub>
            </mtd>
          </mtr>
          <mtr>
            <mtd>
              <mn>0</mn>
            </mtd>
            <mtd>
              <mn>1</mn>
            </mtd>
            <mtd>
              <mn>0</mn>
            </mtd>
          </mtr>
          <mtr>
            <mtd>
              <mo>&#x2212;<!-- − --></mo>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>y</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <mn>0</mn>
            </mtd>
            <mtd>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>y</mi>
                </mrow>
              </msub>
            </mtd>
          </mtr>
        </mtable>
        <mo>]</mo>
      </mrow>
      <mo>=</mo>
      <mrow>
        <mo>[</mo>
        <mtable rowspacing="4pt" columnspacing="1em">
          <mtr>
            <mtd>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>y</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <mo>&#x2212;<!-- − --></mo>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>y</mi>
                </mrow>
              </msub>
            </mtd>
          </mtr>
          <mtr>
            <mtd>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>y</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>y</mi>
                </mrow>
              </msub>
            </mtd>
          </mtr>
          <mtr>
            <mtd>
              <mo>&#x2212;<!-- − --></mo>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>y</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <mn>0</mn>
            </mtd>
            <mtd>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>y</mi>
                </mrow>
              </msub>
            </mtd>
          </mtr>
        </mtable>
        <mo>]</mo>
      </mrow>
      <mspace depth="1cm" />
      <mo linebreak="newline"></mo>
    </mrow>
  </mstyle>
</math>
<math>
  <mstyle displaystyle="true">
    <mrow>
      <msub>
        <mi>R</mi>
        <mrow class="MJX-TeXAtom-ORD">
          <mi>z</mi>
          <mi>y</mi>
          <mi>x</mi>
        </mrow>
      </msub>
      <mo>=</mo>
      <msub>
        <mi>R</mi>
        <mrow class="MJX-TeXAtom-ORD">
          <mi>z</mi>
          <mi>y</mi>
        </mrow>
      </msub>
      <mo>&#x22C5;<!-- ⋅ --></mo>
      <msub>
        <mi>R</mi>
        <mrow class="MJX-TeXAtom-ORD">
          <mi>x</mi>
        </mrow>
      </msub>
      <mo>=</mo>
      <mrow>
        <mo>[</mo>
        <mtable rowspacing="4pt" columnspacing="1em">
          <mtr>
            <mtd>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>y</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <mo>&#x2212;<!-- − --></mo>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>y</mi>
                </mrow>
              </msub>
            </mtd>
          </mtr>
          <mtr>
            <mtd>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>y</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>y</mi>
                </mrow>
              </msub>
            </mtd>
          </mtr>
          <mtr>
            <mtd>
              <mo>&#x2212;<!-- − --></mo>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>y</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <mn>0</mn>
            </mtd>
            <mtd>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>y</mi>
                </mrow>
              </msub>
            </mtd>
          </mtr>
        </mtable>
        <mo>]</mo>
      </mrow>
      <mo>&#x22C5;<!-- ⋅ --></mo>
      <mrow>
        <mo>[</mo>
        <mtable rowspacing="4pt" columnspacing="1em">
          <mtr>
            <mtd>
              <mn>1</mn>
            </mtd>
            <mtd>
              <mn>0</mn>
            </mtd>
            <mtd>
              <mn>0</mn>
            </mtd>
          </mtr>
          <mtr>
            <mtd>
              <mn>0</mn>
            </mtd>
            <mtd>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>x</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <mo>&#x2212;<!-- − --></mo>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>x</mi>
                </mrow>
              </msub>
            </mtd>
          </mtr>
          <mtr>
            <mtd>
              <mn>0</mn>
            </mtd>
            <mtd>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>x</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>x</mi>
                </mrow>
              </msub>
            </mtd>
          </mtr>
        </mtable>
        <mo>]</mo>
      </mrow>
      <mo>=</mo>
      <mrow>
        <mo>[</mo>
        <mtable rowspacing="4pt" columnspacing="1em">
          <mtr>
            <mtd>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>y</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>y</mi>
                </mrow>
              </msub>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>x</mi>
                </mrow>
              </msub>
              <mo>&#x2212;<!-- − --></mo>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>x</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>x</mi>
                </mrow>
              </msub>
              <mo>+</mo>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>y</mi>
                </mrow>
              </msub>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>x</mi>
                </mrow>
              </msub>
            </mtd>
          </mtr>
          <mtr>
            <mtd>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>y</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>x</mi>
                </mrow>
              </msub>
              <mo>+</mo>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>y</mi>
                </mrow>
              </msub>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>x</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>y</mi>
                </mrow>
              </msub>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>x</mi>
                </mrow>
              </msub>
              <mo>&#x2212;<!-- − --></mo>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>z</mi>
                </mrow>
              </msub>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>x</mi>
                </mrow>
              </msub>
            </mtd>
          </mtr>
          <mtr>
            <mtd>
              <mo>&#x2212;<!-- − --></mo>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>y</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>y</mi>
                </mrow>
              </msub>
              <msub>
                <mi>s</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>x</mi>
                </mrow>
              </msub>
            </mtd>
            <mtd>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>y</mi>
                </mrow>
              </msub>
              <msub>
                <mi>c</mi>
                <mrow class="MJX-TeXAtom-ORD">
                  <mi>x</mi>
                </mrow>
              </msub>
            </mtd>
          </mtr>
        </mtable>
        <mo>]</mo>
      </mrow>
      <mspace depth="1cm" />
      <mo linebreak="newline"></mo>
    </mrow>
  </mstyle>
</math>


